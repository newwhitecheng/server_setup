# After browsing through Tensorflow's installation website, I think I can improve it a little bit based on my own experience. 

You can reference to [original set up scrips](https://www.tensorflow.org/install/pip) from tensorflow as site note]

## check your machine's env by
  ```
  python3 --version
  ```

## Install virtual environment for current user if you don't have sudo
You can create virtual environment by either virtualenv or anaconda 

### I prefer create by Anaconda
(I skip the installation of Ananconda here since you'll never get in trouble with that)
```
conda create -n env3.6 python=3.6
```

### But you can also create by virtualenv
install virtualenv
```
python3 -m pip install --user virtualenv
```
create virtual environment 
```
virtualenv --system-site-packages --python=python3.6 env3.6
```
### trouble shooting

```
hc218@hl279-cmp-02:~$ python3 -m pip install --user virtualenv
Collecting virtualenv
  Downloading https://files.pythonhosted.org/packages/8f/f1/c0b069ca6cb44f9681715232e6d3d65c75866dd231c5e4a88e80a46634bb/virtualenv-16.3.0-py2.py3-none-any.whl (2.0MB)
    100% |████████████████████████████████| 2.0MB 16.9MB/s
Requirement already satisfied: setuptools>=18.0.0 in ./anaconda3/lib/python3.7/site-packages (from virtualenv) (40.2.0)
twisted 18.7.0 requires PyHamcrest>=1.9.0, which is not installed.
Installing collected packages: virtualenv
Successfully installed virtualenv-16.3.0
You are using pip version 10.0.1, however version 19.0.1 is available.
You should consider upgrading via the 'pip install --upgrade pip' command.
hc218@hl279-cmp-02:~$ python3 -m pip install --user PyHamcrest
Collecting PyHamcrest
  Downloading https://files.pythonhosted.org/packages/9a/d5/d37fd731b7d0e91afcc84577edeccf4638b4f9b82f5ffe2f8b62e2ddc609/PyHamcrest-1.9.0-py2.py3-none-any.whl (52kB)
    100% |████████████████████████████████| 61kB 3.7MB/s
Requirement already satisfied: six in ./anaconda3/lib/python3.7/site-packages (from PyHamcrest) (1.11.0)
Requirement already satisfied: setuptools in ./anaconda3/lib/python3.7/site-packages (from PyHamcrest) (40.2.0)
Installing collected packages: PyHamcrest
Successfully installed PyHamcrest-1.9.0
You are using pip version 10.0.1, however version 19.0.1 is available.
You should consider upgrading via the 'pip install --upgrade pip' command.
hc218@hl279-cmp-02:~$ python3 -m pip install --user virtualenv
Requirement already satisfied: virtualenv in ./.local/lib/python3.7/site-packages (16.3.0)
Requirement already satisfied: setuptools>=18.0.0 in ./anaconda3/lib/python3.7/site-packages (from virtualenv) (40.2.0)
You are using pip version 10.0.1, however version 19.0.1 is available.
You should consider upgrading via the 'pip install --upgrade pip' command.
```

## For virtualevn, install the Python development environment on your system 
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

## For Anaconda, you can install the Python development environment on your system through

```
conda install python=3.6
```


## Finally we can install the TensorFlow pip package!
For both virtualenv and Anaconda. Install Tensorflow with cpu only by 
```
pip install --upgrade tensorflow
```
Install Tensorflow with gpu by 
```
pip install --upgrade tensorflow-gpu
```

