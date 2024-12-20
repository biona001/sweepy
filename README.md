# sweepy

`sweepy` is a python package for performing the statistical [sweep operation](https://hua-zhou.github.io/teaching/biostatm280-2017spring/slides/11-sweep/sweep.html) on `numpy` matrices. The class `SweepMatrix` is a thin wrapper over numpy `darray`s that can be swept forward or backwards. 

:warning: **This is my hobby project during Christmas 2024. Use at your own risk!** :warning:

## Features

The following operations are supported **in-place** and **allocation-free**:

+ Matrix inversions
+ Computation of determinants
+ Checking of (strict) positive-definiteness
+ Linear regression (beta hat, variance of OLS estimator, residuals)

## Running tests

1. Git clone the repo
2. Install `pytest` via `pip3 install pytest` if you haven't already
3. Execute `pytest tests` in the top level directory of `sweepy`

## Related packages

+ [SweepOperator.jl](https://github.com/joshday/SweepOperator.jl) in Julia
+ [sweep.operator](https://search.r-project.org/CRAN/refmans/fastmatrix/html/sweep.operator.html) in R

## References

+ [Biostats M280 lecture notes at UCLA](https://hua-zhou.github.io/teaching/biostatm280-2017spring/slides/11-sweep/sweep.html)
+ Section 7.4-7.6 of [Numerical Analysis for Statisticians](https://link.springer.com/book/10.1007/978-1-4419-5945-4) by Kenneth Lange (2010). Probably the best place to read about sweep operator.
+ [Blog post by SAS](https://blogs.sas.com/content/iml/2018/04/18/sweep-operator-sas.html)

## TODO
+ CI
+ Docs
+ PyPI
+ Number of download badge
+ Stepwise regression
+ Conditional formulas for MVN
+ MANOVA
+ Support single precision and complex
+ Benchmarks, e.g. timing comparison with `np.inv()` and `np.linalg.lstsq()`
+ Recursive tiling, see https://github.com/joshday/SweepOperator.jl/issues/9
+ Blog post
