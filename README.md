# Quick Start

Ape plugin that allows tracking addresses and contracts in projects and globally.

## Dependencies

- [python3](https://www.python.org/downloads) version 3.8 or greater, python3-dev

## Installation

### via `pip`

You can install the latest release via [`pip`](https://pypi.org/project/pip/):

```bash
pip install ape-addressbook
```

### via `setuptools`

You can clone the repository and use [`setuptools`](https://github.com/pypa/setuptools) for the most up-to-date version:

```bash
git clone https://github.com/ApeWorX/ape-addressbook.git
cd ape-addressbook
python3 setup.py install
```

## Quick Usage

To use the addressbook in a project, add common addresses to your `ape-config.yaml` file like this:

```yaml
addressbook:
  entries:
    shared_account: "0x2192f6112a026bce4047CeD2A16553Fd31E798B6"
```

Then, to use the address, import the addressbook and access it via the alias set in the config:

```python
from ape_addressbook import addressbook

address = addressbook["shared_account"]
```

You can also add global addresses:

```python
from ape_addressbook import addressbook

addressbook.set_global_entry("global_address", "0x2192f6112a026bce4047CeD2A16553Fd31E798B6")
```

## Development

This project is in development and should be considered a beta.
Things might not be in their final state and breaking changes may occur.
Comments, questions, criticisms and pull requests are welcomed.
