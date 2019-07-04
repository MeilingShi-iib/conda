# Conda environment with environment.yml

[![Binder](https://camo.githubusercontent.com/0e31117e59b0f68b809723f2171c3bb252f752d0/687474703a2f2f6d7962696e6465722e6f72672f62616467655f6c6f676f2e737667)](https://mybinder.org/v2/gh/MeilingShi-iib/conda/master)

A Binder-compatible repo with an `environment.yml` file.

Access this Binder at the following URL:

http://beta.mybinder.org/v2/gh/binder-examples/conda_environment/v1.0?filepath=index.ipynb

## Notes
The `environment.yml` file should list all Python libraries on which your notebooks
depend, specified as though they were created using the following `conda` commands:

```
source activate example-environment
conda env export --no-builds -f environment.yml
```

Note that the only libraries available to you will be the ones specified in
the `environment.yml`, so be sure to include everything that you need! 

Also note that conda will possibly try to include OS-specific packages in `environment.yml`, so you
may have to manually prune `environment.yml` to get rid of these packages. Confirmed Mac-OSX-specific
packages that should be removed are:

* libcxxabi=4.0.1
* appnope=0.1.0
* libgfortran=3.0.1
* libcxx=4.0.1
