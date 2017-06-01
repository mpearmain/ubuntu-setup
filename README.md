# ubuntu-setup

A simple script to setup some of my personal settings, get various packages and libraries on a new ubuntu instance.

The crux of this is useful for doing Data Science / Kaggle comps

Mostly R and python in virtual envs.

run `chmod +x run_setup` followed by `sudo run_setup`

Then to get all the virtual ens running use:

```shell
dir_venvs=$HOME"/venv"
dir_venv27="$dir_venvs/python2.7"
dir_venv35="$dir_venvs/python3.5"

echo "creating venv $dir_venv"

virtualenv --python=python2.7 $dir_venv27
virtualenv --python=python3.5 $dir_venv35

source $dir_venv27"/bin/activate"
./_python_packages
deactivate

source $dir_venv35"/bin/activate"
./_python_packages
deactivate

./_R_packages
```
