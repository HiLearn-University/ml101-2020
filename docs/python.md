# We are going to use python3.7 for our class.

Python is very versatile and can be installed in different ways, to make installation easy, we are going to test all our code using Conda environments.
You can download miniconda from [their website](https://docs.conda.io/en/latest/miniconda.html).


## Install Anaconda on linux

* In your browser, download the [Anaconda installer ](https://repo.anaconda.com/archive/Anaconda3-2020.02-Linux-x86_64.sh) for Linux.
* Enter the following to install Anaconda type this to terminal 
```
bash ~/Downloads/Anaconda3-2020.02-Linux-x86_64.sh
```
* answer to all question with yes
* after the installation open a new terminal or type this to terminal
```
source ~/.bashrc
```

* you can:
 - activate `conda activate`
 - deactivate `conda deactivate`
 - show path `which conda`

## Install Anaconda on windows

Install Git Bash (https://git-scm.com/download/win). Please note that during installation you should select the checkbox **Use Git and Optional Unix tools from the Windows Command Prompt**.

Install Anaconda (https://www.anaconda.com/products/individual)

Configuring Git Bash to Run Python

Open Git bash terminal. Write `pwd` to get the path of your home directory. My home directory is /c/Users/USER. If you used default settings Anaconda instalation folder should be /c/Users/USER/Anaconda3. 

Next, enter the following commands in your **git-bash terminal**, replacing[YOUR_PATH] with the path to your Anaconda installation. For example, I would replace [YOUR PATH] in the string below with /c/Users/USER/Anaconda3.

```
echo 'export PATH="$PATH:[YOUR_PATH]:[YOUR_PATH]/Scripts"' >> .bashrc
echo 'alias python="winpty python.exe"' >> .bashrc
source .bashrc
```

Test run
Run the following commands to make sure you can access conda, Python, and the Python interpreter.

```
conda --version
python --version
```


## Creating new environments for each assignment

We recommend you create a new environment for each assignment. We will
specify all the required software in a requirements.txt file, which you
can use to create a new conda environment using:

```
conda create -n assignemtn42 python=3.7 --file requirements.txt
```

After activate the environment
```
conda activate assignemtn42
```

Verify that the environment is activates, by verifying that pytest points to the correct environment
```
$$ which pytest
/home/arsen/miniconda3/envs/assignemtn42/bin/pytest
```

Now you can run tests using pytest by running
```
PYTHONPATH=. pytest
```

