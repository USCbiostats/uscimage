uscimage template package
================

This package provides a set of wrappers to be used with `rmarkdown` in which personalized templates and configurations are set automatically to produce documents for the USC IMAGE project

Installation
------------

Using devtools

``` r
devtools::install_github("USCBiostats/uscimage")
```

Example
-------

For now, we have a template for `beamer_presentation`, which in our case is called `beamer_USCImage`. To use this with your Rmarkdown document, you simply need to set `output: uscimage::beamer_USCImage`. The following example shows this adding an extra option that is passed to `rmarkdown::beamer_presentation`, the `includes` option:

``` rmd
---
title: "My fancy P01 Beamer presentation"
short_title: 
author: "George G. Vega Yon"
date: "October 5, 2017"
institute:
  - Department of Preventive Medicine
  - University of Southern California
short_institute: USC
short_author: Vega Yon
output:
  uscimage::beamer_USCImage:
    includes:
      in_header:
        \def\mytree{some code here}
---
```

Moreover, this package provides extra arguments that the current default beamer template does not hava:

1.  short\_title: Which allows passing the optional short title to `\title[]{}`

2.  short\_institute: Which allows passing the optional short institute names to `\institute[]{}`

3.  short\_author: Which allows passing the optional short authors to `\author[]{}`