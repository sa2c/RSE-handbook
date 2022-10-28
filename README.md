# SA2C RSE Handbook

A way of working guide for the Research Software Engineering team
at the Swansea Academy of Advanced Computing (SA2C).

## Getting started

Before committing changes,
you should install the Git pre-commit hooks.
These are managed using the `pre-commit` framework.
Once you have installed `pre-commit`, you can then use

```sh
    pre-commit install
```

to add the relevant hook to the repository
so that your changes will be checked before they are committed.

This will avoid unnecessary CI failures
due to contributions not passing the linting check.
