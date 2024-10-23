# `calliope-tutorial`

## Getting started

Follow these [installation instructions](https://github.com/sjpfenninger/optimisation-course/blob/main/README.md) to set up a Python environment with everything necessary installed.

Inside a Jupyter Notebook, you can run a model with these two lines of code - the `!` means execution of a tool outside of Python, and you could also run these two commands (without the `!` in a terminal or shell window if you prefer that):

```bash
!calliope run economic_dispatch/model.yaml --save_netcdf results_economic_dispatch.nc
!calligraph results_economic_dispatch.nc
```
