# python-devcontainer-poetry

Starter Python project using Poetry with a dev container.

## Usage

To use this template, click the "Use this template" button on the GitHub page. This will create a new repository with the same files as this one.

Clone your repository and open it in Visual Studio Code. This allows you to use the devcontainer which includes Python and Poetry.

## Getting Started

Create the source directory and test directory:

```bash
mkdir <project-name>
mkdir tests
```

Create a new Python file in the source directory:

```bash
touch <project-name>/__init__.py
touch tests/__init__.py
```

## Setup a project with Poetry

To create a new project with Poetry, run the following command.  Use the `project-name` used above to create the directory as the name of the project:

```bash
poetry init
```

Optional: Add pytest to the dev group. You can do this during the init process or by adding the package later:

```bash
poetry add -G dev pytest
```

## Start poetry shell

```bash
poetry shell
```

## Add Dependencies

```bash
poetry add <package-name>
```

## Install Dependencies

```bash
poetry install
```

## Run Tests With Poetry

```bash
poetry run pytest
```

## Run the application

Create a file called `app.py` in the project directory and add the following code:

```python
def main():
    print("Hello, world!")
    print("This is the main function.")
    
if __name__ == "__main__":
    main()
```

```bash
poetry run python <project-name>/app.py
```

## Build the Package

```bash
$ poetry build
```

## Useful Poetry Commands

* poetry show —Lists the packages installed in your current project’s virtual environment. You can use `poetry show --tree` to view dependencies in a tree format to help understand the hierarchical structure of package dependencies.
* poetry add — Add new dependencies to your project. It automatically updates your pyproject.toml and poetry.lock files.
* poetry install — Reads the pyproject.toml file from the current project, resolves the dependencies, and installs them. If a poetry.lock file exists, it will use the exact versions from there instead of resolving them.
* poetry env — Shows information about the current environment or even removes virtual environments associated with the project.
poetry shell— Spawns a shell, like bash or zsh, within the virtual environment created by Poetry.
* poetry remove— Removes a package that is no longer necessary from the pyproject.toml and lock file.
poetry version minor— Bumps the minor version of your project (according to semantic versioning). Similar for MAJOR or PATCH .