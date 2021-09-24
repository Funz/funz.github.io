---
title: Funz
permalink: /docs/home/
redirect_from: /docs/index.html
---

As a starting point, Funz is the integration of some __numerical engineering tools__ (some that you probably have already used):

* a pre-compilation engine:
    [![parameters cheatsheet]({{ site.baseurl }}/docs/ParameterizingInputFiles.png){:width="400"}]({{ site.baseurl }}/docs/ParameterizingInputFiles.png)
  * __parsing/replacing__ __variables__ for your simulation input files (eg. search '$x' everywhere and replace by an arbitrary numerical value),
  * parsing/replacing variables __formula__ (eg. once '$x' i replaced, evaluate and replace '@{$x +1}' also),
* a loop to __pre-compile__ different arbitrary values of '$x',
* a network protocol to __send/receive__ pre-compiled __input files__ on remote __calculation servers__,
* an output file parser to __extract interest values__,
* a driver to set up arbitrary values of '$x', possibly coming from a __"design of experiments"__ algorithm (optimization, inversion, sensitivity analysis, ...).
    [![algorithm cheatsheet]({{ site.baseurl }}/docs/Algorithm.png){:width="400"}]({{ site.baseurl }}/docs/Algorithm.png)

## Integrated simulation software (plugins)

Simulation softwares are coupled in Funz through __plugins__. Following are available:

* [Excel](https://github.com/Funz/plugin-Excel)
* [Python](https://github.com/Funz/plugin-Python)
* [R](https://github.com/Funz/plugin-R)
* [Modelica](https://github.com/Funz/plugin-Modelica)
* [Cast3M](https://github.com/Funz/plugin-Cast3m)
* [bash](https://github.com/Funz/plugin-Bash)
* [VBS](https://github.com/Funz/plugin-VBS)
* [cmd.exe](https://github.com/Funz/plugin-Cmd.exe)
* [MCNP](https://github.com/Funz/plugin-MCNP)
* [Scale](https://github.com/Funz/plugin-Scale)
* [Cristal](https://github.com/Funz/plugin-Cristal)
* [Telemac](https://github.com/Funz/plugin-Telemac)
* [and more... on GitHub repository](https://github.com/Funz/)

## Integrated design of experiments (algorithms)c

Design of experiments "drivers" are integrated in Funz as standardized '.R' files by GdR MASCOT-NUM. Following are available:

* [Brent](https://github.com/Funz/algorithm-Brent) root finding
* [GradientDescent](https://github.com/Funz/algorithm-GradientDescent) local optimization
* [EGO](https://github.com/Funz/algorithm-EGO) global optimization
* [and more... on GitHub repository](https://github.com/Funz/)

