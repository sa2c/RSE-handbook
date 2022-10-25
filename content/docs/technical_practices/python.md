---
# Page title as it appears in the navigation menu
title: "Python Tools and Practices"
# Adjust weight to reorder menu items (lower numbers appear first)
weight: 3
---

# Python Tools and Practices

If none of the excluding reasons from the general [Tools and Best
Practices](https://sa2c.github.io/RSE-handbook/docs/technical_practices#tools_and_best_practices)
applies, do the following:

- Autoformat your code with [black](https://github.com/psf/black)
- Sort your inputs with [isort](https://pycqa.github.io/isort/)
- Use type hints and [mypy](https://mypy.readthedocs.io/en/stable/) as a static
  type checker
- Lint your code with [flake8](https://flake8.pycqa.org/en/latest/) and
  [pylint](https://pylint.pycqa.org/en/latest/) (they have some overlap but they
  are not identical)
- Use [pytest](https://docs.pytest.org/en/7.2.x/) for automated testing

We might at some point provide more details on how to do that here. It would be
particularly nice to have a [cookiecutter](https://www.cookiecutter.io/)
template to start from. For now, there are existing ones out there that get you
most of the way.
