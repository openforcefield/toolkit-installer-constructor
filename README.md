## Summary

This repository contains the build script for the Open Force Field tookit single-file installers.

_Special thanks to @loriab and the Psi4 community, as this is basically a copy of [their build system](https://github.com/psi4/psi4meta/tree/master/conda-recipes/constructor-cutter-unified)_

## Status

* ~This recipe is active and functional as of 2019-08-01~ This recipe is inactive as of 2021-08-31 (and has been inactive for a while). Instead [this github action](https://github.com/openforcefield/openff-toolkit/blob/da37f07d9f6b19fe5143fbf52fb8d21c8f4517e6/.github/workflows/installer.yml) in the openff-toolkit repo is used to make the installers. 
* We do not yet have permission from OpenEye to include the `openeye-toolkits` conda package in the installer.

## Usage


* run in an environment that has `cookiecutter` installed. `constructor` must also be accessible.

* edit `cookiecutter/cookiecutter.json` for control. edit `cookiecutter/{{.../construct.yaml` for templating

* dir `build/` is regenerated each time.

* may want to clear out ~/.conda/constructor

* `python run.py`

* watch out for `py_` in buildstring as this means a noarch, which can be troublesome
