---
title: Installation
permalink: /docs/install/
---

### Manual install (bundle)

For conveniency, many integrated packages are available, bundled with plugins and algorithms in GH releases:

* [Excel](https://github.com/Funz/plugin-Excel/releases/latest)
* [Python](https://github.com/Funz/plugin-Python/releases/latest)
* [R](https://github.com/Funz/plugin-R/releases/latest)
* [Modelica](https://github.com/Funz/plugin-Modelica/releases/latest)
* [Cast3M](https://github.com/Funz/plugin-Cast3m/releases/latest)
* [VBS](https://github.com/Funz/plugin-VBS/releases/latest)
* [MCNP](https://github.com/Funz/plugin-MCNP/releases/latest)
* [Scale](https://github.com/Funz/plugin-ScaleThen/releases/latest)
* [Cristal](https://github.com/Funz/plugin-Cristal/releases/latest)
* [Telemac](https://github.com/Funz/plugin-Telemac/releases/latest)
* [Jupyter](https://github.com/Funz/plugin-Telemac/releases/latest)
* [Rmd](https://github.com/Funz/plugin-Telemac/releases/latest)

You can get 'Funz-*.zip' archive of whole working Funz directory, unzip and just follow [usage guidelines]({{ "/docs/usage_cli/" | prepend: site.baseurl }}).

### Manual install (from scratch)

If you prefer a custom installation, you can 

* start with one of the quite-scratch distributions:
  * e.g. for Windows: [get Funz-Cmd.exe.zip](https://github.com/Funz/plugin-Cmd.exe/releases/latest)
  * e.g. for Linux & OSX: [get Funz-Bash.zip](https://github.com/Funz/plugin-Bash/releases/latest)
* test that it works properly with example files (available in 'samples' directory)
* then add some other plugins you need:
  * get 'plugin-*.zip' file in any of the previous GH releases
  * unzip in 'Funz' directory
* add some algorithms you need:
  * get 'algorithms-*.zip' file in any of the previous GH releases
  * unzip in 'Funz/plugins/doe' directory
