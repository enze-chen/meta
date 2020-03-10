# Projects

The following projects fit together to form the Executable Book Project tool chain. 

```{contents} Contents:
```

## Overview

High level feature lists are provided as a simple measure of progress. 

1. `Phase 1` are items required for minimal viable product, 
1. `Phase 2` include items that are planned for initial release, and 
1. `Phase 3` captures wishlist items to be implemented in the future.

A component / interface diagram for the project:

```{image} _static/ebp-project-flowchart-version3.png
```

## Parsers

### [myst-parser](https://github.com/ExecutableBookProject/MyST-Parser)

**Project Type:** Internal

**Description:** An extended commonmark compliant parser, with bridges to docutils/sphinx

**Coordinator:** [Chris Sewell](https://github.com/chrisjsewell)

**Features:**

*Phase 1:*

- [x] `myst` parser that is compliant with commonmark as a base, with extensions for roles and directives. For supported syntax please refer to [here](https://github.com/ExecutableBookProject/MyST-Parser#parsed-token-classes)

*Phase II:*

- [ ] footnote support
- [ ] integration with `myst-nb` 

### [myst-nb](https://github.com/ExecutableBookProject/MyST-NB)

**Project Type:** Internal

**Description:** Enables sphinx to read IPYNB files that contain
myst based syntax

**Coordinator:** [Chris Holdgraf](https://github.com/choldgraf)

**Features:**

*Phase 1:*

- [x] parse `ipynb` files that contain `myst` syntax.
- [ ] integration with `myst-parser`
- [ ] integration with `jupyter-cache`
- [ ] build additional nodes (mimebundle) for `HTML` and `LaTeX` builders

*Phase II:*

- [ ] build custom LaTeX Builder


## Jupyter Notebook Execution

### [jupyter-cache](https://github.com/ExecutableBookProject/jupyter-cache) [Internal]

**Description:** Provide caching and execution control for a
collection of Jupyter notebooks.

**Features:**

*Phase 1:*

- [ ] provide cache for a set of notebooks to track changes
- [ ] execute notebooks and save outputs

*Phase II:*

- [ ] parallel execution of notebooks
- [ ] support for notebook file dependencies (i.e. assets such as data files, images)

*Phase III:*

- [ ] support to specify `ipynb` execution ordering and dependency

## Build Tools

### Command Line Tool (jupyterbook)

**Project Type:** Internal

**Description:** Enable unified command line tool to coordinate the underlying packages and building targets using `sphinx`

## Authoring Tools

### [JupyterText](https://github.com/mwouts/jupytext)

**Project Type:** External Project

**Description:** Jupyter Notebooks as Markdown Documents, Julia, Python or R scripts

**Contribution:** 

The primary aim is to add myst to jupytext to enable *bi-directional* conversion 
between IPYNB and myst text based files. 

A seconday objective is to understand how JupyText may be used to convert between 
ipynb and myst files in realtime to enable joint editing between the 
two formats. 

**Coordinator:** [Aakash](https://github.com/AakashGfude)