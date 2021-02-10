.. image:: https://img.shields.io/badge/lse--439-lsst.io-brightgreen.svg
   :target: https://lse-439.lsst.io
.. image:: https://github.com/lsst/lse-439/workflows/CI/badge.svg
   :target: https://github.com/lsst/lse-439/actions/

############################
LSST Science Validation Plan
############################

LSE-439
=======

This document describes the Science Validation Plan for the Rubin Obsevatory Legacy Survey of Space and Time (LSST) 

Links
=====

- Live drafts: https://lse-439.lsst.io
- GitHub: https://github.com/lsst/lse-439

Build
=====

This repository includes lsst-texmf_ as a Git submodule.
Clone this repository::

    git clone --recurse-submodules https://github.com/lsst/lse-439

Compile the PDF::

    make

Clean built files::

    make clean

Updating acronyms
-----------------

A table of the technote's acronyms and their definitions are maintained in the ``acronyms.tex`` file, which is committed as part of this repository.
To update the acronyms table in ``acronyms.tex``::

    make acronyms.tex

*Note: this command requires that this repository was cloned as a submodule.*

The acronyms discovery code scans the LaTeX source for probable acronyms.
You can ensure that certain strings aren't treated as acronyms by adding them to the `skipacronyms.txt <./skipacronyms.txt>`_ file.

The lsst-texmf_ repository centrally maintains definitions for LSST acronyms.
You can also add new acronym definitions, or override the definitions of acronyms, by editing the `myacronyms.txt <./myacronyms.txt>`_ file.

Updating lsst-texmf
-------------------

`lsst-texmf`_ includes BibTeX files, the ``lsstdoc`` class file, and acronym definitions, among other essential tooling for LSST's LaTeX documentation projects.
To update to a newer version of `lsst-texmf`_, you can update the submodule in this repository::

   git submodule update --init --recursive

Commit, then push, the updated submodule.

.. _lsst-texmf: https://github.com/lsst/lsst-texmf
