- # OS
	- ## MacOS
		- [Homebrew — The Missing Package Manager for macOS (or Linux)](https://brew.sh)
		- `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
	- ## Windows
		- WSL
		- Native?
	- ## Linux
		- All set!
# Python dependencies
	- [Home · pyenv/pyenv Wiki · GitHub](https://github.com/pyenv/pyenv/wiki#suggested-build-environment)
	- ## MacOS
		- `brew install openssl readline sqlite3 xz zlib tcl-tk`
	- ## Linux
		- ```shell
		  sudo apt update; sudo apt install build-essential libssl-dev zlib1g-dev \
		  libbz2-dev libreadline-dev libsqlite3-dev curl \
		  libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev \
		  liblzma-dev
		  ```
# Pyenv
	- [GitHub - pyenv/pyenv: Simple Python version management](https://github.com/pyenv/pyenv)
	- ```python
	  echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
	  echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
	  echo 'eval "$(pyenv init -)"' >> ~/.bashrc
	  ```
	- Restart shell: `exec "$SHELL"`
	- `which pyenv`
	- Commands
		- `pyenv versions`
		- `pyenv install -l`
		- `pyenv global <version>`
# Poetry
	- [Poetry - Python dependency management and packaging made easy](https://python-poetry.org)
	- `pip install poetry`
	- Add `export PATH=$PATH:$HOME/.poetry/bin` to .bashrc
	- ```shell
	  poetry new -n --src hello-world
	  ```
	- `poetry add numpy`
	- `poetry env info`
	- `poetry env info --path`
	- `python` -> `import numpy as np` -- fails
	- `poetry run python` -> `import numpy as np` -- passes
- # VSCode
	- `Ctrl+Shift+P`
	- Install `Python` extension
	- Configure `Python`
	- Configure Tests
	- Configure `settings.json`
		- "files.exclude": {
			- `**/__pycache__`
			- `**/.pytest_cache`
		- }