# Getting started if you don't know how to use Python and Jupyter Notebooks

This file is for people who are still early in learning Python, Jupyter notebooks, and the terminal/command line.

See this video for a walkthrough of the content.

Related files (week 1 content):
- `Python_basics.ipynb`
- `Python_Functions_Tutorial.ipynb`

## Install Python 3
If you don't have Python installed, [Anaconda](https://www.anaconda.com/download) is easiest to install.  Preferably use Python 3, not Python 2.  Python 3 has better handling for unicode (a type of text encoding).  Python 2 is also being sunset (no longer suppported) in 2020.  If you already have Python 2 installed on your system, you could use it, but it's not recommended.  One option to install Python 3 is to install Ubuntu 18.04 LTS (or the latest LTS version) under [virtualbox](https://www.lifewire.com/run-ubuntu-within-windows-virtualbox-2202098), which will avoid potential problems of using both Python 2 and 3 on the same system.

Another better option is to create anaconda environments with different versions of Python. For example, creating a Python2 environment (from the command line -- command prompt or terminal):

`conda create --name py2_env python=2.7`

or python 3:

`conda create -n py3_env python=3.6`

Then getting into and out of the environment works like:

`conda activate py3_env`
`conda deactivate`

See these links for more info: [link 1](https://salishsea-meopar-docs.readthedocs.io/en/latest/work_env/python3_conda_environment.html), [link 2](https://uoa-eresearch.github.io/eresearch-cookbook/recipe/2014/11/20/conda/).

## Run Jupyter notebooks

Download the `.ipynb` file(s) under the week 1 content, navigate to the folder where you downloaded it (it’s suggested to make a folder for this course), then type 'jupyter notebook' from the terminal or command prompt.  Here are some basics on command prompts/terminals if you need refreshing or learning:

- [Windows](https://www.digitalcitizen.life/command-prompt-how-use-basic-commands)
- [Mac](https://mac.appstorm.net/how-to/utilities-how-to/how-to-use-terminal-the-basics/)

[DataCamp](https://www.datacamp.com) has an intro and beginners Python course you might consider going through if you don’t know Python very well.  This should take about 4 hours per course.

[Kaggle](https://www.kaggle.com/learn/overview) also has a free Python course.

There is also a Jupyter notebook under the week 1 content (`Python_basics.ipynb`) you can go through as a Python/Jupyter notebook refresher or learning experience.  Or DataCamp also has a [Jupyter notebook tutorial](https://www.datacamp.com/community/tutorials/tutorial-jupyter-notebook). For all assignments, we will do them in Jupyter notebooks and export PDFs.  There is another file, `Python_Functions_Tutorial.ipynb` which can help you learn functions in Python if you're not familiar.

Lastly, here are some getting started with Jupyter notebooks videos:
- [Windows](https://youtu.be/epaC7PCtWxk)
- [Mac/Linux](https://youtu.be/xYuUrHOAE5Y)

## Optional: Install NLTK and the stopwords
There are at least 3 sources for stopwords: NLTK, sklearn, and SpaCy.  If you want to use NLTK, here is how.

Install NLTK with either `pip install NLTK` or `conda install NLTK`.  Then download the `stopwords` list.  Start a Python session: either a jupyter notebook, an IPython session by typing `ipython` from your command line, or a plain Python session by typing `Python` from the command line.  Then import NLTK, and either open the GUI or download `stopwords` directly:

```python
import nltk
nltk.downlaod()  # opens GUI
nltk.download('stopwords')  # downloads stopwords directly
from nltk.corpus import stopwords  # test that it works
print(stopwords)
```