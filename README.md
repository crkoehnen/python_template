# python template

This is a template for a basic python program.

# From Scratch

## Make a project folder

```bash
mkdir python_template
```

```bash
cd python_template
```

## Initialize pyenv

```bash
python -m venv .venv
```

Activate:

```bash
PS C:\Users\ik3377pp\temp\foo> .\.venv\Scripts\activate
(.venv) PS C:\Users\ik3377pp\temp\foo>
```

## Install pytest (and friends).

```bash
pip install pytest
```

## Create requirements.txt

```bash
pip freeze > requirements.txt
```

## Open folder in vscode

```bash
code .
```

## Make src and test folders

```bash
mkdir ./src
mkdir ./test
```

## Create ./src/hello.py

```python

def double(x):
    return x * 2

def main():
    print('hello, world')

main()
```

Create an empty __init__.py file:

```bash
touch src/__init__.py
```

You should be able to test with:

```bash
(.venv) PS C:\Users\ik3377pp\temp\foo> python -m src.hello
hello, world
```

## Create ./test/hello_test.py

```python
from src.hello import double

def test_double_zero():
    assert(double(0) == 0)
```

Create test/__init__.py

```bash
touch test/__init__.py
```

You should be able to run the test with:

```bash
(.venv) PS C:\Users\ik3377pp\temp\foo> python -m pytest
======================================================= test session starts ========================================================
platform win32 -- Python 3.12.7, pytest-8.3.2, pluggy-1.5.0
rootdir: C:\Users\ik3377pp\temp\foo
collected 1 item

test\test_hello.py .                                                                                                          [100%]

======================================================== 1 passed in 0.01s =========================================================
```

## git

### Create an empty repo on github.

### Create a file called, .gitignore
```
.pytest_cache
.venv
__pycache__
```

Introduce the project to git.

```bash
git init
```

Set the remote using the instructions from the github repo.  Something like,

```bash
git remote add origin <github-project>
```

Add the files to git.

```bash
git add .
```

Commit the files

```bash
git commit -m "initial commit"
```

Push the files

```bash
git push origin main
```

# From a Clone

## Clone

```bash
git clone <github-project>
```

## rename the folder

```bash
mv <folder> <new-project-name>
```

## Delete .git

In windows:
```bash
Remove-Item -Path .git -Recurse -Force
```

On Linux or a Mac:
```bash
rm -rf .git
```

## Add to Github under a new name.

Follow the same steps as the "git" section as if you were creating the project from scratch.

