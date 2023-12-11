# Fitchi

Haplotype genealogies based on Fitch distances.

This is a Python package for [Fitchi](https://github.com/mmatschiner/Fitchi). For more information on the original, see [here](https://evoinformatics.group/fitchi.html).

[![Genealogy](images/genealogy.png)](https://itaxotools.github.io/Fitchi/examples/example.html)

[*Click for comprehensive output example*](https://itaxotools.github.io/Fitchi/examples/example.html)

## Installation

Fitchi is available on PyPI. You can install it through `pip`:

```
pip install itaxotools-fitchi
```

## Usage

The original command-line tool is included as part of the installation. It produces HTML files from Nexus files, as demonstrated with the [example input and ouput files here](./examples/). For information about the available options, you may refer to the [original documentation](https://evoinformatics.group/fitchi.html).

You will need *all* dependencies in order to run Fitchi this way:

```
fitchi examples/example.nex examples/example.html  -m 3 -p pop1 pop2
```

You may also invoke Fitchi from Python using `compute_fitchi_tree()`. This returns a tree in the form of `HaploNode` objects, which can be used for downstream analysis or visualization. Only scipy is required in this case.

See the [scripts](./scripts/) folder for some usage examples.

## Dependencies

Fitchi requires [scipy](https://pypi.org/project/scipy/).
Extra statistics require [biopython](https://pypi.org/project/biopython/).
Visualization requires [pygraphviz](https://pypi.org/project/pygraphviz/).

To install pygraphviz, please follow the [instructions](https://pygraphviz.github.io/documentation/stable/install.html) from the pygraphviz documentation.
For example, to install pygraphviz on Windows, having installed [Graphviz](https://graphviz.org/download/) to the default location, execute the following command in PowerShell:
```
pip install pygraphviz --config-setting build_ext^="^--include-dir=C:\Program Files\Graphviz\include" --config-setting build_ext^="^--library-dir=C:\Program Files\Graphviz\lib"
```

## Citation

*Matschiner M (2015) Fitchi: Haplotype genealogy graphs based on the Fitch algorithm. Bioinformatics, 32:1250-252.*
