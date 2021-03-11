Tweedieverse: Differential analysis of multi-omics data based on the Tweedie distribution
================
Himel Mallick
2021-03-11

-   [Introduction](#introduction)
-   [Installation](#installation)
-   [Basic Usage](#basic-usage)
-   [Input](#input)
-   [Output](#output)
-   [Tutorials](#tutorials)
-   [Citation](#citation)
-   [Issues](#issues)

Introduction
------------

Tweedieverse is an R package for differential analysis of multi-omics data. Tweedieverse implements a range of statistical methodology based on the [Tweedie distributions](https://en.wikipedia.org/wiki/Tweedie_distribution).

Unlike traditional single-omics tools, Tweedieverse is technology-agnostic and can be applied to both count and continuous measurements arising from diverse high-throughput technologies (e.g. transcript abundances from bulk and single-cell RNA-Seq studies in the form of UMI counts or non-UMI counts, microbiome taxonomic and functional profiles in the form of counts or relative abundances, and compound abundance levels or peak intensities from metabolomics and other mass spectrometry-based experiments, among others).

The software includes multiple analysis methods (e.g. self-adaptive, zero-inflated, and non-zero-inflated statistical models) as well as multiple customization options such as the inclusion of random effects and multiple covariates along with several data exploration capabilities and visualization modules in a unified estimation umbrella.

Installation
------------

To install the latest release version of `Tweedieverse` from [CRAN](https://cran.r-project.org/) (**not yet available**) run the following command:

``` r
install.packages("Tweedieverse")
library(Tweedieverse)
```

Alternatively, the latest development version of `Tweedieverse` can be loaded using the following command (execute from within a fresh R session):

``` r
install.packages('devtools')
library(devtools)
devtools::install_github("himelmallick/Tweedieverse")
library(Tweedieverse)
```

After installing `Tweedieverse`, please make sure the following package versions are also installed (a prerequisite for zero-inflated Tweedie models):

``` r
devtools::install_version("statmod", version = "1.4.33", repos ="http://cran.us.r-project.org")
```

``` r
devtools::install_version("cplm", version = "0.7-8", repos = "http://cran.us.r-project.org")
```

Basic Usage
-----------

``` r
Tweedieverse(features, metadata, output)
```

Input
-----

Tweedieverse requires two input files:

-   **features**: A data frame of 'omics features such as taxa, genes, transcripts, metabolites, etc.
-   **metadata**: A data frame of metadata to be associated.

For full options, check out the reference manual or type `?Tweedieverse` in your R console.

Output
------

A data frame containing coefficient estimates, p-values, and q-values (multiplicity-adjusted p-values) are returned, along with other parameter estimates from the fitted per-feature models.

Tutorials
---------

1.  [Differential expression of scRNA-Seq UMI counts](https://github.com/himelmallick/tweedieverse/) (To be updated) <br/>
2.  [Differential expression of scRNA-Seq non-UMI counts](https://github.com/himelmallick/tweedieverse/) (To be updated) <br/>
3.  [Differential expression analysis of bulk RNA-Seq counts](https://github.com/himelmallick/tweedieverse/) (To be updated) <br/>
4.  [Differential analysis of microbiome relative abundances](https://github.com/himelmallick/tweedieverse/) (To be updated) <br/>
5.  [Differential analysis of metabolite abundances](https://github.com/himelmallick/tweedieverse/) (To be updated)

Citation
--------

If you use `Tweedieverse` in your work, please cite the following papers:

Mallick H et al. (2021+). Differential Expression of Single-cell RNA-seq Data using Tweedie Models. (In Submission).

Mallick H et al. (2021+). Tweedieverse - A Unified Statistical Framework for Differential Analysis of Multi-omics Data. (In Submission).

Issues
------

We are happy to troubleshoot any issues with the package. Please contact the maintainer via email or [open an issue](https://github.com/himelmallick/tweedieverse/issues) in the GitHub repository.
