references:
https://medium.com/bettercode/how-to-build-a-modern-ci-cd-pipeline-5faa01891a5b
https://docs.python-guide.org/starting/install3/osx/
https://docs.python-guide.org/dev/virtualenvs/#virtualenvironments-ref

Setup Your MAC OS Developement Environment
==========================================
- Install 'Homebrew' on your MAC to manage packages for you
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

- Insert the Homebrew directory at the top of your PATH environment variable. 
You can do this by adding the following line at the bottom of your ~/.profile file:
$ export PATH="/usr/local/opt/python/libexec/bin:$PATH"

Setup Your Python Environment
=============================
- Install Python3 (Using 'brew' will make Python3 your DEFAULT automatically)
$ brew install python
$ python --version
Python 3.7.7

- Install Python Package Manager, PyPI or pip3:
Homebrew installs pip3 pointing to Python3 for you.
$ pip --version
pip 20.0.2 from /usr/local/lib/python3.7/site-packages/pip (python 3.7)

- Install (User mode) Python Virtual Environment, venv:
Three ways to create virtual environment:
1 - pipenv (preferred)
pipenv is a dependency manager for Python projects.
$ pip install pipenv --user

2 - virtualenv
$ pip install virtualenv --user

3 - venv (least common)
Unlike the first two, does not need a separate package.
$ python -m venv .

$ pip show pipenv
Name: pipenv
Version: 2020.6.2

$ pip show virtualenv
Name: virtualenv
Version: 20.0.25

- Add this line to your $PATH in ~/.bashrc:
export PATH="/Users/daryushzavvar/Library/Python/3.7/bin:$PATH"
$ virtualenv --version
virtualenv 20.0.25 from /Users/daryushzavvar/Library/Python/3.7/lib/python/site-packages/virtualenv/__init__.py
ERROR:root:SystemExit: 0

- Check what you have installed in your environment:
$ pip freeze
WARNING: Could not generate requirement for distribution -irtualenv 20.0.25 (/usr/local/lib/python3.7/site-packages): Parse error at "'-irtuale'": Expected W:(abcd...)
appdirs==1.4.4
certifi==2020.6.20
distlib==0.3.1
filelock==3.0.12
importlib-metadata==1.7.0
pipenv==2020.6.2
six==1.15.0
virtualenv==20.0.25
virtualenv-clone==0.5.4
zipp==3.1.0


- need 'pytest' framework to run the test.
	- to install 'pytest', we use Python Virtual Environment ('virtualenv').
	- to check if you have 'virtualenv' do:
		[]$ virtualenv venv
		[]$ source venv/bin/activate
		(venv) []$
		... -> find the rest in the link above


