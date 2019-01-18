# After browsing through Tensorflow's installation website, I think I can improve it a little bit based on my own experience. 

## check your machine's env by
  ```
  python3 --version
  ```

## Install the Python development environment on your system 
0. tf website only said python 2 or 3 but 3.6 and 3.7 makes difference
1. Go to https://www.python.org/
2. Choose the correct python version according to tensorflow build. For example python3.6
3. Download and install python3.6
4. Create a new virtual environment by choosing a Python interpreter and making a ./venv directory to hold it:
by using the following commmand
```
virtualenv --system-site-packages --python=python3.6 env3.6
```
5. Activate the virtual environment using a shell-specific command:
```
source ./env3.6/bin/activate
```
6. And to exit virtualenv later:

```
source ./env3.6/bin/activate
```

## Finally we can install the TensorFlow pip package!
1. Install Tensorflow with cpu only
```
pip install --upgrade tensorflow
```
