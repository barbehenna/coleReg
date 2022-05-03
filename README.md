# ColeReg: COmpound Loss Emporium with Regression

This project is an R "sub-package" containing nonparametric regression methods for the simultaneous estimation of normal means under squared error loss. `ColeReg` was used in the development of the methods accompanying [A nonparametric regression approach to asymptotically optimal estimation of normal means (2022)](https://doi.org/10.48550/arXiv.2205.00336); however, these methods have been integrated into [sdzhao/cole](https://github.com/sdzhao/cole) and are **maintained here for reference only**. 

## Functions

- `wtf1()` implements the constrained and penalized least-squares estimator, $\hat{d}$ in the paper. To support this function we offer two different optimizers: MOSEK and CVXR, and three different methods to select the tuning parameter: high-probability upper bound, plug-in, and cross-validation (`TV1.oracle.highprob()`, `TV1.oracle.plugin()`, and `cv.wtf1()`, respectively)
- `wtf0()` implements the monotone-only least-squares estimator given bandwidth $h$, $\tilde{d}_h$ in the paper. The bandwidth rate achieving asymptotically optimal risk is used by default. A fast, accurate approximation is used for the knots by default; however, `optimal.knots()`, gives the best knots for the risk estimate.
- `f.kde()` implements Brown and Greenshtein's $f$-estimator (https://www.jstor.org/stable/30243684) with their suggested bandwidth as default.
