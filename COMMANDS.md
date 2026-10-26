# Command Log — Robust NER in Noisy Text

This file records the terminal commands used to build, run, test, and maintain this project.

For each new milestone, add the commands here with a short explanation.

---

## 1. Check installed tools

```cmd
python --version
git --version
```

- `python --version`: Displays the installed Python version.
- `git --version`: Displays the installed Git version.

## 2. Create the project and initialize Git

```cmd
mkdir robust-ner-noisy-text
cd robust-ner-noisy-text
git init
```

- `mkdir`: Creates a directory.
- `cd`: Changes the current directory.
- `git init`: Initializes a local Git repository.

## 3. Create project folders

```cmd
mkdir src
mkdir notebooks
mkdir tests
mkdir reports
```

- `src`: Python source code.
- `notebooks`: Experiments and analysis.
- `tests`: Automated tests.
- `reports`: Experiment reports and results.

## 4. Create a Python virtual environment

```cmd
python -m venv .venv
```

Creates an isolated Python environment in `.venv`.

### Activate in Windows Command Prompt

```cmd
.venv\Scripts\activate.bat
```

### Activate in PowerShell

```powershell
.\.venv\Scripts\Activate.ps1
```

PowerShell may block activation depending on its execution policy. Command Prompt is an alternative.

### Verify the environment

```cmd
python --version
python -m pip --version
```

A `(.venv)` prefix in the terminal indicates that the environment is activated.

## 5. Install project dependencies

```cmd
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

- `python -m pip`: Runs pip using the selected Python interpreter.
- `--upgrade pip`: Updates pip.
- `-r requirements.txt`: Installs the packages listed in the requirements file.

## 6. Verify machine-learning libraries

```cmd
python -c "import torch, transformers, datasets, evaluate, seqeval; print('PyTorch:', torch.__version__); print('Transformers:', transformers.__version__); print('CUDA available:', torch.cuda.is_available()); print('All core libraries imported successfully!')"
```

Checks whether core libraries import successfully and whether PyTorch detects CUDA.

## 7. Track changes with Git

```cmd
git status
git add .
git commit -m "Describe the change"
git log -1 --oneline
```

- `git status`: Shows changed and untracked files.
- `git add .`: Stages changes in the current repository.
- `git commit`: Saves a snapshot of staged changes.
- `git log -1 --oneline`: Shows the latest commit.

Review `git status` before using `git add .` to avoid staging unintended files.

## 8. Connect and push to GitHub

```cmd
git remote -v
git branch -M main
git push -u origin main
```

- `git remote -v`: Displays configured remote repositories.
- `git branch -M main`: Renames the current branch to `main`.
- `git push -u origin main`: Pushes the branch to GitHub and sets its upstream.

The remote repository must be configured before pushing.

## 9. Future project commands

Add commands here as we introduce them, including:

- Dataset downloading and inspection.
- Tokenization and label alignment.
- Model training and evaluation.
- Noise generation.
- Experiment tracking and result analysis.

---

**Rule:** Record each important command, its purpose, and an example output or common error when useful.
