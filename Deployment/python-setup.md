# Setting Up a Python Development Environment on Windows

## 1. Overview

Python is a versatile language used for web development, data science, and automation. A professional setup requires more than just installing the language; it involves managing multiple versions and isolating project dependencies using virtual environments.

## 2. Audience

This guide is for Python developers who want to move beyond basic scripts and build maintainable projects. It is suitable for those transitioning from other languages or starting fresh on Windows.

## 3. Prerequisites

* Windows 10/11.

* A code editor (Visual Studio Code is recommended).

* Stable internet connection.

## 4. System Requirements

* RAM: Minimum 4 GB.

* Storage: 500 MB for basic installation; more for libraries like Pandas or TensorFlow.

## 5. Install Python via Official Installer

1. Download the latest stable release from python.org.

2. Critical Step: Check the box "Add Python to PATH" before clicking "Install Now."

3. Disable the "Path Length Limit" at the end of the installation if prompted.

4. Verify the installation:

```powershell
    python --version
    pip --version
```

## 6. Configure Virtual Environments (venv)

Directly installing libraries into your global Python folder causes version conflicts. Always use a virtual environment for every project.

Step 1: Create a project directory

```powershell
mkdir my-python-project
cd my-python-project
```
Step 2: Create the environment

```powershell
python -m venv venv
```
Step 3: Activate the environment

```powershell
.\venv\Scripts\activate
```
Your terminal should now show (venv) before the command prompt.

## 7. Manage Dependencies with Pip

Once the environment is active, use pip to install packages locally to that project.

* Install a package: pip install requests

* Generate a requirements file: pip freeze > requirements.txt (Essential for sharing your project).

* Install from a file: pip install -r requirements.txt

## 8. Conclusion

Setting up a dedicated environment for Python on Windows ensures that your development workflow remains organized and scalable. By utilizing virtual environments and requirements files, you protect your system-wide Python installation and make it easy for others to reproduce your work without dependency errors.