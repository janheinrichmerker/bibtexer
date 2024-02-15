[![CI status](https://img.shields.io/github/actions/workflow/status/heinrichreimer/bibtexer/ci.yml?branch=main&style=flat-square)](https://github.com/heinrichreimer/bibtexer/actions/workflows/ci.yml)
[![Maintenance](https://img.shields.io/maintenance/yes/2024?style=flat-square)](https://github.com/heinrichreimer/bibtexer/graphs/contributors)  
[![Issues](https://img.shields.io/github/issues/heinrichreimer/bibtexer?style=flat-square)](https://github.com/heinrichreimer/bibtexer/issues)
[![Pull requests](https://img.shields.io/github/issues-pr/heinrichreimer/bibtexer?style=flat-square)](https://github.com/heinrichreimer/bibtexer/pulls)
[![Commit activity](https://img.shields.io/github/commit-activity/m/heinrichreimer/bibtexer?style=flat-square)](https://github.com/heinrichreimer/bibtexer/commits)
[![License](https://img.shields.io/github/license/heinrichreimer/bibtexer?style=flat-square)](LICENSE)

# 📚 bibtexer

An opinionated BibTeX file cleaner for computer science.

## Goals

- BibTeX files as input and output
- Clean format, ready to be published
- Supplement bibliographic data from [DBLP](https://dblp.org/) and [CrossRef](https://crossref.org/)
- Adhere to [natbib](https://ctan.org/pkg/natbib) and [BibLaTeX](https://ctan.org/pkg/biblatex) standards
- Short identifiers to favor typing efficiency
- Favor a simple CLI over a fancy GUI
- BibTeX is the single source of truth
- Permissive license

## Conventions

- Favor DOIs over URLs
- Shorten journal names as per [TODO](somestandard)
- Use conference acronyms instead of full names:
  - Preceded with `Proceedings of`
- Identifiers in the form of `lastname:YYYY[x]`:
  - `lastname` is the last name of the first author, without diacritics
  - `YYYY` is the four-digit year of publication
  - `[x]` is an optional one-letter suffix (e.g., `a`, `b`, etc.) in case the same first author has published more than one paper in a year.
- arXiv papers are `@misc` entries

## Installation

Install [Python 3.10](https://python.org/downloads/) or higher and [pipx](https://pypa.github.io/pipx/installation/) (this allows you to install the BibTeXer CLI in a virtual environment).
Then, you can install the BibTeXer CLI by running:

```shell
pipx install bibtexer
```

If you do not want to use pipx, you can also install this tool with standard pip:

```shell
pip install --user bibtexer
```

## Usage

Now you can run the CLI by running:

```shell
bibtexer --help
```

## Development

First, install [Python 3.10](https://python.org/downloads/) or higher and then clone this repository.
From inside the repository directory, create a virtual environment and activate it:

```shell
python3.10 -m venv venv/
source venv/bin/activate
```

Then, install the test dependencies:

```shell
pip install -e .[tests]
```

After having implemented a new feature, please check the code format, inspect common LINT errors, and run all unit tests with the following commands:

```shell
ruff .                         # Code format and LINT
mypy .                         # Static typing
bandit -c pyproject.toml -r .  # Security
pytest .                       # Unit tests
```

## Contribute

If you have found a bug in this tool or feel like some feature is missing, please create an [issue](https://github.com/heinrichreimer/bibtexer/issues). We also gratefully accept [pull requests](https://github.com/heinrichreimer/bibtexer/pulls)!

If you are unsure about anything, post an [issue](https://github.com/heinrichreimer/bibtexer/issues/new) or contact us:

- [heinrich.reimer@uni-jena.de](mailto:heinrich.reimer@uni-jena.de)

We are happy to help!

## Similar projects

> TODO

- [bibcleaner](https://github.com/sirrice/bibcleaner)
- [bibcure](https://github.com/bibcure/bibcure)
- [tidybib](https://github.com/ntessore/tidybib)
- [bibtex-dblp](https://github.com/volkm/bibtex-dblp)
- [imbibed](https://github.com/cassiersg/imbibed)
- [regenbib](https://github.com/joachimneu/regenbib)
- [autobiber](https://github.com/Yeba/autobiber)

## License

This repository is released under the [MIT license](LICENSE).
