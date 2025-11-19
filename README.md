# workflow-python-lint
In the repo settings, open Branches, add a rule for main, and enable Require a pull request before merging.

The workflow in this repository will fail if the python code does not pass a lint test (black)
or any of the tests fail.

# workflow-python-lint
In the repo settings, open Branches, add a rule for main, and enable Require a pull request before merging.

The workflow in this repository will fail if the python code does not pass a lint test (black)
or any of the tests fail.

## Developer setup

If you want to develop locally and have VS Code format Python on save using Black, follow these steps on Windows (PowerShell):

1. Install Python from https://www.python.org/downloads/windows/ and enable "Add Python to PATH" during installation.

2. Open a new PowerShell and verify Python is available:

```powershell
py --version
```

3. Install development dependencies (Black and pytest):

```powershell
py -3 -m pip install --user -r requirements-dev.txt
```

4. In VS Code select the Python interpreter that has Black installed (click the interpreter in the status bar).

5. The repository includes workspace settings in `.vscode/settings.json` which enable `editor.formatOnSave` and set the Python formatter to Black. If you prefer to enable format-on-save globally, open Settings and search for "Format On Save".

If you prefer an isolated environment, create and use a virtual environment instead:

```powershell
py -3 -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements-dev.txt
```

