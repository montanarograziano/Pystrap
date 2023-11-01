# Pystrap
A simple python template to boostrap your next project 🚀

## The purpose
Pystrap aims at simplyfing all the necessary (and redundant) steps needed during the setup of a python project.

I find myself doing the same actions everytime I start a new python project, and so I thought _why not automate it?_

The idea is create a CLI and package it so that it can be used with something like `pystrap init`, but for now just cloning the repo would be sufficient and running the necessary instructions would be sufficient.

 ## What it does

The repository contains a typical standard structure for a python project, organized as follows:
```sh
├── pyproject.toml
├── requirements.txt
├── Pipfile
├── README.md
├── docs/
├── src/
└── tests/
```

The three main folders are:
- **src/** -> Contains the source code.
- **tests/** -> Contains the code used for testing.
- **docs** -> Contains the documentation.

## Documentation settings
The tool I use to build the documentation is [mkdocs-material](https://squidfunk.github.io/mkdocs-material/). It works **mkdocs.yml** file which can be used to configure the theming, navigation and other plugins. Markdown code can be places inside the **docs** folder.



## Managing dependencies
To manage dependencies, I like to use [pipenv](https://pipenv.pypa.io/en/latest/): it's a tool similar to Poetry and it works using a Pipfile with all the dependencies listes inside.
Therefore, the only real dependency in the *requirements.txt* is **Pipenv**.

To create a Pipenv virtual environment, simply run `pipenv install` and it will create a new one inside the already existing `.venv` folder.

The command will install all the dependencies inside the Pipfile. To install a new package (and add it to the Pipfile), simply run:

`pipenv install packagename`

To activate the virtual environment, run `pipenv shell`.

## Pyproject.toml settings
*Pyproject.toml* is used to manage project-scoped information and settings for specific tools such as **ruff**.

Those can be tuned to your preferences and thanks to the **pyproject.toml** file they can be shared allowing consistency for the whole team.

## Future works
- [ ] Add *pre-commit* script and config.
- [ ] Add a minimal CI template.
