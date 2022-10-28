---
# Page title as it appears in the navigation menu
title: "Python Tools and Practices"
# Adjust weight to reorder menu items (lower numbers appear first)
weight: 5
---

# Python Tools and Practices

If none of the excluding reasons
from the general [Tools and Best Practices][tools-and-best-practices] applies,
do the following:

- Autoformat your code with [black][black]
- Sort your inputs with [isort][isort]
- Use type hints and [mypy][mypy] as a static type checker
- Lint your code with [flake8][flake8] and [pylint][pylint]
  (they have some overlap but they   are not identical)
- Use [pytest][pytest] for automated testing

We might at some point provide more details on how to do that here.
It would be particularly nice to have a [cookiecutter][cookiecutter] template
to start from.
For now, there are existing ones out there that get you most of the way.

[black]: <https://github.com/psf/black>
[cookiecutter]: <https://www.cookiecutter.io/>
[flake8]: <https://flake8.pycqa.org/en/latest/>
[isort]: <https://pycqa.github.io/isort/>
[mypy]: <https://mypy.readthedocs.io/en/stable/>
[pylint]: <https://pylint.pycqa.org/en/latest/>
[pytest]: <https://docs.pytest.org/en/7.2.x/>
[tools-and-best-practices]: {{< relref "/docs/technical_practices#tools-and-best-practices" >}}
