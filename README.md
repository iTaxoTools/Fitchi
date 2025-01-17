# Fitchi

[![PyPI - Version](https://img.shields.io/pypi/v/itaxotools-fitchi?color=tomato)](
    https://pypi.org/project/itaxotools-fitchi)
[![PyPI - Python Version](https://img.shields.io/pypi/pyversions/itaxotools-fitchi)](
    https://pypi.org/project/itaxotools-fitchi)
[![GitHub - Tests](https://img.shields.io/github/actions/workflow/status/iTaxoTools/Fitchi/test.yml?label=tests)](
    https://github.com/iTaxoTools/Fitchi/actions/workflows/test.yml)

Haplotype genealogies based on Fitch distances.

This is a Python package for [Fitchi](https://github.com/mmatschiner/Fitchi). For more information on the original, see [here](https://evoinformatics.group/fitchi.html).

[![Genealogy](https://raw.githubusercontent.com/iTaxoTools/Fitchi/main/images/genealogy.png)](
    https://itaxotools.github.io/Fitchi/examples/example.html)

[*Click for a comprehensive output example*](
    https://itaxotools.github.io/Fitchi/examples/example.html)

## Installation

Fitchi is available on PyPI. You can install it through `pip`:

```
pip install itaxotools-fitchi
```

## Usage

The original command-line tool is included as part of the installation. It produces HTML files from Nexus files, as demonstrated with the [example input and output files](https://github.com/iTaxoTools/Fitchi/tree/main/examples). For information about the available options, you may refer to the [original documentation](https://evoinformatics.group/fitchi.html).

Note that you will need *all* dependencies in order to run Fitchi this way:

```
fitchi examples/example.nex examples/example.html -m 3 -p pop1 pop2
start examples/example.html  # browse results on Windows
```

You may also invoke Fitchi from Python using `compute_fitchi_tree()`. This returns a tree in the form of `HaploNode` objects, which can be used for downstream analysis or visualization. Only scipy is required in this case.

See the [scripts](https://github.com/iTaxoTools/Fitchi/tree/main/scripts) folder for some usage examples.

## Dependencies

Fitchi requires [scipy](https://pypi.org/project/scipy/).
Extra statistics require [biopython](https://pypi.org/project/biopython/).
Visualization requires [pygraphviz](https://pypi.org/project/pygraphviz/).

To install pygraphviz, please follow [these](https://pygraphviz.github.io/documentation/stable/install.html) instructions from the pygraphviz documentation.
For example, to install pygraphviz on Windows, first install [Graphviz](https://graphviz.org/download/) to the default location, then execute the following command in PowerShell:
```
pip install pygraphviz --config-setting build_ext^="^--include-dir=C:\Program Files\Graphviz\include" --config-setting build_ext^="^--library-dir=C:\Program Files\Graphviz\lib"
```

## Citation

*Matschiner M (2015) Fitchi: Haplotype genealogy graphs based on the Fitch algorithm. Bioinformatics, 32:1250-252.*
