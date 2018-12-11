# CS109 Best Practices & Recommendation Systems
****
## [Link to Slides](https://github.com/cs109/2015/blob/master/Lectures/13-BestPractices_Recommendations.pdf)


****
# Pycon 2015 Lecture
## Recommendation Systems
****
## [Link to YouTube](https://youtu.be/F6gWjOc1FUs)
## [Link to Slides](https://github.com/PyCon/2015-slides)
## [Link to Presenter's Static Page](http://unatainc.github.io/pycon2015/)
    - The datasets and IPython Notebooks can be downloaded from here
# Presentation starts at 8:12

Pandas Series and DataFrames - Lecture and Questions

# Loading the MovieLens dataset 49:30

`pd.read_table()` for loading the .dat files

# Challenge prep: evaluation mechanism 55:50

# Minimal Recommendation Engine v1.0:
## Simple mean ratings
### 1:13:30

- Content-based filtering using mean ratings

# After Break 1:29:00

## Pandas Groupby & Pivoting Ends 1:42:00

# Implicit simularity function

# Custom Similarity Functions 2:10:00

****
# PyData 2017
## Coding Best Practices
****
### [Video Link](https://youtu.be/nFVjLSvK5po)

- **Code Stubs** will assist in organization and ensure that the most efficient and productive functions are utilized. [Link](https://youtu.be/nFVjLSvK5po?t=864)
- **The right tool for the job** will ensure that you are not wasting your time on trained models or APIs that are already out there. [Link](https://youtu.be/nFVjLSvK5po?t=1109)
    - It may be worth your while to investigate some of these
- **Create your own stock of Gists** These code snippets will make you more efficient than searching for examples [Link](https://youtu.be/nFVjLSvK5po?t=1561)
- **PEP 20** Do not forget the Zen of Python [Link](https://www.python.org/dev/peps/pep-0020/)

****
# SciPy 2016
## Data Science is Software
****
### [Video Link](https://youtu.be/EKUy0TSLg04)
### [Presentation Resources Link](https://github.com/drivendata/data-science-is-software)

- `tqdm` package is useful for progress bars in long running `for` loops
- **Project Structure** [Link](https://youtu.be/EKUy0TSLg04?t=953) [Resource](https://drivendata.github.io/cookiecutter-data-science)
- **Refactoring Interactive Notebooks to Code** Then codify the entire process [Link](https://youtu.be/EKUy0TSLg04?t=1653)
- **Minimum Reproducible Environment** [Link](https://youtu.be/EKUy0TSLg04?t=2171)
    - The watermark extension is the bare minimum for providing environment information
    - `.` is the shorthand for `source` in UNIX when activating different environments
    - `pip` install trick [Link](https://youtu.be/EKUy0TSLg04?t=2740) 
        ```python
        pip install -r requirements.txt
        ```
    - `pip freeze > new-requirements.txt`
- **Separation of configuration** 12-factor app principles [Link](https://youtu.be/EKUy0TSLg04?t=2978)
    `dotenv` is a package that handles these environment variables
- **Debugging Techniques** [Link](https://youtu.be/EKUy0TSLg04?t=3590)
    - Talk out your code
    - Do not copy and paste. If this seems necessary, write a function
- **Creating Python Packages**[Link](https://youtu.be/EKUy0TSLg04?t=4527)
    - pip install -e *directory*
- **Debug Magic Function** `%debug` [Link](https://youtu.be/EKUy0TSLg04?t=4875)
    - `u` moves up a level in the command stack. You can move up till you get to your code
    - Then run your code and debug to find the fix
    - `q` will quit the debugger
    
    - `%pdb 1` will instantiate the debugger console every time an error is thrown in your code
    - `%pdb 0` will turn off the debugger
- **Code profiling**
    - `%prun` "profile run" provides a popup
- **Debugging Integrated Development Environment**
    - PyCharm
- **Testing** - unittest -- pytest
    - `engarde` package is a way to declare your expectations
    - `coverage.py` 
    - a "fixture" is known data that is used for only testing `@pytest.fixture`
- **The Joel Test**
- **Version Control**
    - Detail your issues and the workflow for addressing them
    - Feature branches
    - Git flow
    - Continuous Integration
    
****
# Constructive Code Review
## @ErikRose
### [Video Link](https://youtu.be/iNG1a--SIlk)
****

# Pycon 2017
- Our comments in code review need to be durable and consistent over time
    - No outdating links. If you are going to link, link to a specific commit
    - What time will the edit be done? When checking progress, be specific of the requirements and expectations
- **Clarity of Explanation**
    - Code
    - Links
    - Higher-bandwidth communications
    - Write down the results!
- **Clarity of Expectation**
- **Tact Hacks** - The Question Mark ... You, We, & This ... Compliments ... Humor
- **AntiPatterns** 
    - prose overview of patch
    - long commit messages
    - small commits
    - comments, docstrings, naming
- **GitX** - breakup changes into multiple commits
- **FileMerge** - Comes packaged with Xcode and is a great tool for checking your diffs
- **Nitpicks** - need to check your self-confidence
- **Python Enhancer Proposals** - PEP 8, PEP 257, Pocco style guide, Sphinx
- **Linters** - flake8
- **Turnarounds**
    - Energizing
    - Comprehensiveness not required
    - Working memory
    - Quick "no's"
- **Feeling Short on Time**
    - Lower standards
    - Never sleep
    - Or pace, prioritize, and peace
![TimeAlgorithm](https://s3-us-west-2.amazonaws.com/schellenbergers3bucket/Time+Decision+Tree.png)
    - **The 2-Minute Rule**
    - Patch-batching
    - Leveling up newcomers (1 -> 2 -> 3 ----> Superstar)
- **The Trust Bank**
    - Never eat lunch alone
    - Say what you feel
![Checklist](https://s3-us-west-2.amazonaws.com/schellenbergers3bucket/Review+Checklist.png)

****
# Getting Started Testing
## [Presenter's Notes](https://nedbatchelder.com/text/test0.html)
## [Video Link](https://youtu.be/FxSsnHeWQBY)
****

# PyCon 2014
- Automated testing is the best way we know how to find out if code works
    - Know if your code works
    - Save time
    - Better code
    - Remove Fear
1. Growing tests
2. `unittest` module
3. Mocks

- **Growing Complication** Testing becomes complicated quickly
    - Independent tests for each code snippet
        - **Tests will grow** - in complexity
        - **Real programs** - are required to run tests in the way we want
        - **Real engineering** - tests will become an engineering problem
        - **Handle common issues in standard ways**
- **`unittest`** is the programmatic solution to this problem [Link](https://youtu.be/FxSsnHeWQBY?t=617)
    - *Good tests* are:
        - Automated
        - Fast
        - Reliable
        - Informative
        - Focused
    - Example:
    ```python
    # test_port1.py
    
    import unittest
    from portfolio1 import Portfolio
    
    class PortfolioTest(unittest.TestCase):
        def test_buy_one_stock(self):
            p = Portfolio()
            p.buy("IBM", 100, 176.48)
            assert p.cost() == 17648.0
    ```
    
    ```python
    $ python -m unittest test_port1
    ```
    - `-m` in the terminal code will run the code in the module specified (`unittest`). And `unittest` knows how to find the code to test by looking for `test_` in the method.
    - Under the hood, `unittest` is running `try:`, `except`, `else:` processes.
    - **Assert Helpers** [Link](https://youtu.be/FxSsnHeWQBY?t=960)
    ```python
    def test_buy_one_stock(self):
        p = Portfolio()
        p.buy("IBM", 100, 176.48)
        self.assertEqual(p.cost(), 17648.0)
    ```
    - When the assertion fails we get more debugging information [Link](https://youtu.be/FxSsnHeWQBY?t=1030)
    - **Pro Tip** Make your own base class [Link](https://youtu.be/FxSsnHeWQBY?t=1038)
    - **Assert Raises** for checking TypeErrors [Link](https://youtu.be/FxSsnHeWQBY?t=1228)
    - **Repetition in your tests** use the setup method [Link](https://youtu.be/FxSsnHeWQBY?t=1303)
        - Also tearDown
        - Also "fixtures" *something to look into*
- **Mocks** [Link](https://youtu.be/FxSsnHeWQBY?t=1405)
    - **Test Doubles** will replace large and slow code dependencies with small and light standins
    - **Coverage reports** what code was not tested? 
    - **Even Better** mock objects [Link](https://youtu.be/FxSsnHeWQBY?t=1761)
    - **Test doubles**
        - Powerful: isolates code
        - Focuses tests
        - Removes speed bumps and randomness
        - BUT: fragile tests!
        - Also: "dependency injection" *something to look into*
- **Tools** [Link](https://youtu.be/FxSsnHeWQBY?t=1929)
    - **addCleanup** nicer than tearDown
    - **doctest** only for testing docs!!!
    - **nose, py.test** better test runners
    - **ddt** data-driven tests
    - **coverage** you'll wonder how you lived without it
    - **Selenium** in-browser testing
    - **Jenkins, Travis** run tests all the time
- **Topics** [Link](https://youtu.be/FxSsnHeWQBY?t=1987)
    - **TDD** tests before code!?
    - **BDD** describe external behaviour
    - **integration tests** bigger chunks
    - **load testing** how much traffic is OK?
    - others, I'm sure...

****
# Python Debugging
## [Video Link](https://youtu.be/04paHt9xG9U)
## [Presenter Resources](https://github.com/krother/talks/tree/master/500speeches)
****

- **Assertion Errors** How do we find the source of an `assert` error? [Link](https://youtu.be/04paHt9xG9U?t=2015)
```python
import pdb; pdb.set_trace()
```
- `l` where are you in the code
- `n` executes the next line
- `s` executes the function
- `dir()`
- `locals()`
- `b` breakpoint `b 68` break at line 68
- `c` continue
- `q` quit
- **conditional breakpoints** [Link](https://youtu.be/04paHt9xG9U?t=2780)
```python
b 69, length != sum(aa_counts)
```

- **Other Tools** - try, except
    - count
    - tests
    - linter
    
- **Logging** [Link](https://youtu.be/04paHt9xG9U?t=4266)

****
# Deploying Python models to production
## [Video Link](https://youtu.be/f3I0izerPvc)
****

### PyData 2017

- Jenkins, Docker [Link](https://youtu.be/f3I0izerPvc?t=515), Kubernetes [Link](https://youtu.be/f3I0izerPvc?t=704), Heapster and ELK [Link](https://youtu.be/f3I0izerPvc?t=1023), Kibana, custom Flask app, custom json logger, Process D > T > A > P [Link](https://youtu.be/f3I0izerPvc?t=1486)

****
# Introduction to Spark with Python
## [Link to Video](https://youtu.be/9xYfNznjClE)
## [Git Repo PyCon 2015](https://github.com/okaram/spark-pycon15)
****

- Resilient Distributed Datasets [Link](https://youtu.be/9xYfNznjClE?t=186)
- Funtional Programming tools in Python [Link](https://youtu.be/9xYfNznjClE?t=546)
- Flatmap [Link](https://youtu.be/9xYfNznjClE?t=1642)
- Now with Spark [Link](https://youtu.be/9xYfNznjClE?t=1907)
- `sc.parallize` will generate a RDD
- If you see a wall of text from Spark logging, you will need to update the profile document. There is a starting draft in the directories provided on the GitHub repo for this video.
- Some RDD methods [Link](https://youtu.be/9xYfNznjClE?t=3034)
    - Transformations
    - Actions
- Read files [Link](https://youtu.be/9xYfNznjClE?t=3314)
- Tuples and ReduceByKey -- Like SQL GroupBy [Link](https://youtu.be/9xYfNznjClE?t=3678)
- Sending Programs with Shell [Link](https://youtu.be/9xYfNznjClE?t=4734)
- Importing local modules .py files [Link](https://youtu.be/9xYfNznjClE?t=4911)
- Joins [Link](https://youtu.be/9xYfNznjClE?t=5486)
- Writing spark applications [Link](https://youtu.be/9xYfNznjClE?t=6335)
- Other Functions [Link](https://youtu.be/9xYfNznjClE?t=6429)
    - Sample()
    - Union, intersection, distinct
    - Coalesce, repartition
    - aggregateByKey
    - groupByKey
    - repartitionAndSortWithinPartitions
    - mapPartitions, mapPartitionsWithIndex
- **New DataTable functionality** [Link](https://youtu.be/9xYfNznjClE?t=6581)
- We now use a SQL context instead of a spark context
- DataTable methodes [Link](https://youtu.be/9xYfNznjClE?t=7291)
- **You can do SQL** [Link](https://youtu.be/9xYfNznjClE?t=7881)
- Performance Considerations [Link](https://youtu.be/9xYfNznjClE?t=8620)
- End of Talk -- Questions -- Slideshow ends with a discussion of Spark over Hadoop [Link](https://youtu.be/9xYfNznjClE?t=9002)