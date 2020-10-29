# Github Action to install Poetry

_**THIS ACTION IS NOT MAINTAINED. USE https://github.com/snok/install-poetry INSTEAD!**_

<p align="left">
  <a href="https://github.com/dschep/install-poetry-action"><img alt="GitHub Actions status" src="https://github.com/dschep/install-poetry-action/workflows/PR%20Checks/badge.svg"></a>
</p>

This action sets up a poetry for use in actions by:

- installing a version of poetry and adding to PATH.

# Usage

See [action.yml](action.yml)

Basic:
```yaml
steps:
- uses: actions/checkout@master
- uses: actions/setup-python@v1
- uses: dschep/install-poetry-action@v1.3
- run: poetry run my_script.py
```

With a specific version:
```yaml
- uses: dschep/install-poetry-action@v1.3
  with:
    version: 1.0.0a1
```

Or use the preview release (not compatible with the `version` option)
```yaml
- uses: dschep/install-poetry-action@v1.3
  with:
    preview: true
```

By default, the Poetry option virtualenvs.create is set to `false`. If you would
like Poetry to create a new virtual environment if one doesn't already exist:
```yaml
- uses: dschep/install-poetry-action@v1.3
  with:
    create_virtualenvs: true
```

# License

The scripts and documentation in this project are released under the [MIT License](LICENSE)

# Contributions

Contributions are welcome!  See [Contributor's Guide](docs/contributors.md)
