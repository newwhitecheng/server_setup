## After browsing through Tensorflow's installation website, I think I can improve it a little bit based on my own experience. 
0. check your machine's env by
  ```
  python3 --version
  ```

1. Install the Python development environment on your system (tf website only said python 2 or 3 but 3.6 and 3.7 makes difference)
* Go to https://www.python.org/
* Choose the correct python version according to tensorflow build. For example python3.6
* Download and install python3.6

2. Create a new virtual environment by choosing a Python interpreter and making a ./venv directory to hold it:
by using the following commmand
```
virtualenv --system-site-packages -p --python=python3.6 ./env3.6
```
