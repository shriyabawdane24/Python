# Python Learning - Day 1

## Python versions with pyenv

[`pyenv`](https://github.com/pyenv/pyenv) helps manage and select between multiple Python versions. This is useful when different projects need different versions.

### pyenv commands

| Command | What it does |
| --- | --- |
| `pyenv versions` | Lists the Python versions managed by pyenv. The active version is usually marked with `*`. |
| `pyenv shell <version>` | Selects a version for the current terminal session. For example, `pyenv shell 3.15.2` selects Python 3.15.2 until the session ends or the selection is changed. |
| `pyenv local <version>` | Selects a version for the current directory and its subdirectories. For example, `pyenv local 3.14.9` creates or updates a `.python-version` file in that directory. |
| `pyenv global <version>` | Sets the default version for directories without a local version. The last global version selected in my command history was 3.15.2. |

When multiple selections apply, a shell-specific selection normally takes precedence over a local selection, which takes precedence over the global selection. In my setup, `app` was assigned Python 3.14.9 locally, while the global version was ultimately set to Python 3.15.2. An active `pyenv shell` selection may temporarily override both.

### Other terminal commands

| Command | What it does |
| --- | --- |
| `python --version` | Displays the version selected for the `python` command. |
| `python3 --version` | Displays the version selected for the `python3` command. Depending on the operating system and PATH configuration, `python3` may resolve differently from `python`. |

This project contains a small introductory Python script in `main.py`. It demonstrates basic output, variables, and reading text from the user.

## What `main.py` does

1. Prints the title `Python Learning - Day1`.
2. Defines two variables: `var1` stores the name `"Shriya"` and `var2` stores the number `33`.
3. Prints the `Basics of Python` heading, then displays the values of both variables.
4. Prompts the user to enter their name and stores the response in `name`.
5. Prints the entered name on its own, then greets the user in two ways:
   - Using `print` with separate values: `Hey <name>`
   - Joining text with the `+` operator: `Hi <name>`

## Run it

From this folder, run:

```bash
python main.py
```

The script will wait for you to enter a name in the terminal.
