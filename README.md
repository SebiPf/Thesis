# Thesis Sebastian Pfeiffer

tbd

## Prerequisites

First we need to download and install Python 3 from [python.org](https://www.python.org/downloads/). The recommended
version is `3.10.7` or above. To inspect the currently installed version we can use the following terminal command:

```shell
python --version
```

*Ensure that the correct version is used in the terminal as well as the selected interpreter.*

---

Usually the dependency management tool `pip` is included in the Python installation. If it is not, download and install
it from [pip.pypa.io](https://pip.pypa.io/en/stable/installation/). Version `19.3` or above is recommended. We can again
use a terminal command to check the version:

```shell
pip --version
```

## Getting started with Python

A great selection of useful resources are:

- [https://www.python.org/about/gettingstarted/](https://www.python.org/about/gettingstarted/)
- [https://docs.python.org/3/tutorial/](https://docs.python.org/3/tutorial/)
- [https://code.visualstudio.com/docs/python/python-tutorial](https://code.visualstudio.com/docs/python/python-tutorial)

## Setting up the development environment

The source code is developed using VS Code. You can use any IDE, but VS Code will be used in the lecture. You can
download VS Code from [https://code.visualstudio.com/][vsc-website]. On Linux you can follow the instructions on
[this][vsc-linux] page. On Arch based systems you can use the OSS version `code` ([Link][vsc-arch-oss]) or the fully
featured proprietary version `visual-studio-code-bin` ([Link][vsc-arch-bin]) from AUR.

### VS Code extensions

- Python `ms-python.python`: Python support in VS Code ([Link][vsc-ext-python])
- Pylance `ms-python.vscode-pylance`: Python language server ([Link][vsc-ext-pylance])
- Python Image Preview `076923.python-image-preview`: You can quickly check your Python image data during debugging
  ([Link][vsc-ext-img-preview])
- Todo Tree `Gruntfuggly.todo-tree`: Provides an overview about all code lines marked with "TODO"
  ([Link][vsc-ext-todo-tree])

### Python VENVs

To more easily develop Python code it is recommended to setup a VENV (virtual environment). In the project root folder
execute the following terminal command:

```shell
python -m venv .venv
```

The will create the hidden folder `.venv` in your current project folder. Next we need to enable the VENV. The VENV will
only be active for the current terminal session. So closing the terminal and re-opening it, will disable the VENV.
Always make sure to enable it before you start developing.

```shell
# For Windows use
.venv\Scripts\Activate.ps1

# For Linux
source .venv/bin/activate
```

Special care is needed when using Windows. Please consult the following [guide][venv-guide] for more information.

---

On both Operation Systems the VENV can be deactivated with the following terminal command:

```shell
deactivate
```

### Installing dependencies

Installing the required dependencies is straight forward:

```shell
pip install .
```

This will load the defined dependencies in `pyproject.toml` and install them inside the VENV.

## Helpful resources

### Python

You can use https://docs.python.org/3/ as a starting point and the [Library Reference][py-lib-ref] or the
[Language Reference][py-lang-ref] should contain all the needed information.

### NumPy

OpenCV uses NumPy `ndarrays` as the common format for data exchange. It can create, operate on, and work with NumPy
arrays. For some operations it makes sense to import the NumPy module and use special functions provided by NumPy.
Other libraries like TensorFlow and SciPy also use NumPy. See the official [docs][numpy-docs] for the API reference.

[venv-guide]: https://docs.python.org/3/library/venv.html
[py-lib-ref]: https://docs.python.org/3/library/index.html
[py-lang-ref]: https://docs.python.org/3/reference/index.html
[numpy-docs]: https://numpy.org/doc/stable/reference/index.html

[vsc-ext-python]: https://marketplace.visualstudio.com/items?itemName=ms-python.python
[vsc-ext-pylance]: https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance
[vsc-ext-img-preview]: https://marketplace.visualstudio.com/items?itemName=076923.python-image-preview
[vsc-ext-todo-tree]: https://marketplace.visualstudio.com/items?itemName=Gruntfuggly.todo-tree

[vsc-website]: https://code.visualstudio.com/
[vsc-linux]: https://code.visualstudio.com/docs/setup/linux
[vsc-arch-oss]: https://archlinux.org/packages/community/x86_64/code/
[vsc-arch-bin]: https://aur.archlinux.org/packages/visual-studio-code-bin