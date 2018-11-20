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

****