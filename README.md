# Python

Here’s a comprehensive list of Python CLI commands and techniques, including specific tools and configurations for PyCharm and Python 3.

### **Python CLI Commands**

#### **1. Python Version Management**

- **Check Python version:**
  ```bash
  python --version
  python3 --version
  ```

- **Update Python (using `pyenv` for version management):**
  ```bash
  pyenv install <version> # Install specific version
  pyenv global <version> # Set global Python version
  pyenv local <version> # Set local Python version
  ```

- **List installed Python versions (using `pyenv`):**
  ```bash
  pyenv versions
  ```

- **List available Python versions (using `pyenv`):**
  ```bash
  pyenv install --list
  ```

#### **2. Python Script Execution**

- **Run a Python script:**
  ```bash
  python script.py
  python3 script.py
  ```

- **Run a script with additional arguments:**
  ```bash
  python script.py arg1 arg2
  ```

- **Run Python in interactive mode:**
  ```bash
  python
  python3
  ```

- **Run Python with debugging:**
  ```bash
  python -m pdb script.py
  ```

- **Run a script with specific environment variables:**
  ```bash
  ENV_VAR=value python script.py
  ```

#### **3. pip (Python Package Installer) Commands**

- **Install a package:**
  ```bash
  pip install package-name
  pip3 install package-name
  ```

- **Install a package from a `requirements.txt` file:**
  ```bash
  pip install -r requirements.txt
  ```

- **Uninstall a package:**
  ```bash
  pip uninstall package-name
  ```

- **List installed packages:**
  ```bash
  pip list
  ```

- **Show details of a specific package:**
  ```bash
  pip show package-name
  ```

- **Update a package to the latest version:**
  ```bash
  pip install --upgrade package-name
  ```

- **Check for outdated packages:**
  ```bash
  pip list --outdated
  ```

- **Freeze the current environment’s packages to a file:**
  ```bash
  pip freeze > requirements.txt
  ```

- **Check for vulnerabilities in installed packages (using `safety`):**
  ```bash
  pip install safety
  safety check
  ```

#### **4. Virtual Environments**

- **Create a virtual environment:**
  ```bash
  python -m venv venv
  python3 -m venv venv
  ```

- **Activate the virtual environment:**
  ```bash
  source venv/bin/activate # Unix/macOS
  .\venv\Scripts\activate # Windows
  ```

- **Deactivate the virtual environment:**
  ```bash
  deactivate
  ```

- **Remove a virtual environment:**
  ```bash
  rm -rf venv # Unix/macOS
  rmdir /s /q venv # Windows
  ```

#### **5. Python Advanced Commands**

- **Run Python with optimizations:**
  ```bash
  python -O script.py
  ```

- **Compile Python scripts to bytecode:**
  ```bash
  python -m py_compile script.py
  ```

- **Compile Python scripts to an executable (using `PyInstaller`):**
  ```bash
  pip install pyinstaller
  pyinstaller --onefile script.py
  ```

- **Generate a profile of your Python code’s performance (using `cProfile`):**
  ```bash
  python -m cProfile script.py
  ```

- **Generate a code coverage report (using `coverage`):**
  ```bash
  pip install coverage
  coverage run script.py
  coverage report
  ```

#### **6. Python Debugging**

- **Start debugging with `pdb` (Python Debugger):**
  ```bash
  python -m pdb script.py
  ```

- **Set a breakpoint in your code:**
  ```python
  import pdb; pdb.set_trace()
  ```

- **Debug with `ipdb` (IPython Debugger):**
  ```bash
  pip install ipdb
  python -m ipdb script.py
  ```

#### **7. Python Testing**

- **Run tests with `unittest`:**
  ```bash
  python -m unittest discover
  ```

- **Run tests with `pytest`:**
  ```bash
  pip install pytest
  pytest
  ```

- **Run tests with `nose`:**
  ```bash
  pip install nose
  nosetests
  ```

#### **8. Code Quality and Linting**

- **Lint Python code with `flake8`:**
  ```bash
  pip install flake8
  flake8 script.py
  ```

- **Lint Python code with `pylint`:**
  ```bash
  pip install pylint
  pylint script.py
  ```

- **Format Python code with `black`:**
  ```bash
  pip install black
  black script.py
  ```

- **Check code formatting with `pylint`:**
  ```bash
  pylint --max-line-length=88 script.py
  ```

#### **9. Python Package Development**

- **Create a new package template:**
  ```bash
  python setup.py sdist
  ```

- **Build a package:**
  ```bash
  python setup.py sdist bdist_wheel
  ```

- **Upload a package to PyPI:**
  ```bash
  pip install twine
  twine upload dist/*
  ```

- **Download a package from PyPI:**
  ```bash
  pip download package-name
  ```

#### **10. Python Environment Management**

- **Set environment variables:**
  ```bash
  export ENV_VAR=value # Unix/macOS
  set ENV_VAR=value # Windows
  ```

- **Use `.env` files with `python-dotenv`:**
  ```bash
  pip install python-dotenv
  ```

  In `script.py`:
  ```python
  from dotenv import load_dotenv
  load_dotenv()
  ```

### **PyCharm-Specific Commands and Features**

#### **1. Command-Line Interface**

- **Run PyCharm from the command line:**
  ```bash
  pycharm # or pycharm64, depending on your installation
  ```

- **Open a project in PyCharm from the command line:**
  ```bash
  pycharm /path/to/project
  ```

- **Open a file in PyCharm from the command line:**
  ```bash
  pycharm /path/to/file.py
  ```

#### **2. PyCharm Integration with Python CLI**

- **Configure a Python interpreter in PyCharm:**
  - Go to `File > Settings > Project > Python Interpreter`
  - Add or select the interpreter (Python 2.x or 3.x)

- **Use PyCharm's Terminal to execute commands:**
  - Open the Terminal tab within PyCharm to run Python commands, `pip` commands, and other shell commands.

- **Run configurations and debugging in PyCharm:**
  - Create and manage run/debug configurations through `Run > Edit Configurations`.
  - Use breakpoints and the integrated debugger to step through code.

- **Manage Python environments in PyCharm:**
  - Create and manage virtual environments via `File > Settings > Project > Python Interpreter > Add`.

#### **3. PyCharm Commands**

- **Install a package in PyCharm’s Terminal:**
  ```bash
  pip install package-name
  ```

- **Check package versions and dependencies within PyCharm:**
  - Use the "Project Interpreter" settings to view and manage packages.

### **Summary**

This extensive list covers fundamental and advanced Python CLI commands, including package management, virtual environments, debugging, testing, and code quality. It also includes PyCharm-specific commands and features for effective development and environment management within PyCharm.
