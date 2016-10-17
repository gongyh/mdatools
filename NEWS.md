v.0.8.0
=======
* tutorial has been moved from GitBook to Bookdown and fully rewritten
* GitHub repo for the package has the tutorial as a static html site in `docs` folder
* the `mdaplot()` and `mdaplotg()` were rewritten completely and now are more easy to use (check tutorial)
* new color scheme 'jet' with jet colors
* new plot type (`'d'`) for density scatter plot
* support for `xlas` and `ylas` in plots to rotate axis ticks
* support for several data attributes to give extra functionality for plots (including manual x-values for line plots)
* rows and columns can be now hidden/excluded via attributes
* factor columns of data frames are now converted to dummy variables automatically when model is created/applied
* scores and loadings plots show % of explained variance in axis labels
* biplot is now available for PCA models (`plotBiplot()`)
* scores plot for PCA model can be now also shown with color grouping (`cgroup`) if no there is no test set
* cross-validation in PCA and PLS has been improved to make it faster
* added a posibility to exclude selected rows and columns from calculations 
* added support for images (check tutorial)

v.0.7.2
=======
* corrected a typo in title of selectivity ratio plot 
* `prep.autoscale()` now do not scale columns with coefficient of variation below given threshold

v.0.7.1
=======
* fixed an issue lead to plot.new() error in some cases
* documentation was regenerated with new version of Roxygen
* file People.RData was renamed to people.RData
* NIPALS method for PCA has been added
* code optimization to speed calculations up

v.0.7.0
=======
* interval PLS variable selection (iPLS) is implemented
* normalization was added to preprocessing methods (`prep.norm`)
* method `getRegcoeffs` was added to PLS model
* automatic selection of optimal components in PLS (Wold's criterion and first local min)
* parameter `cgroup` for plots now can work with factors correctly (including ones with text levels)
* all documentation was converted to roxygen2 format
* NAMESPACE file is generated by roxygen2
* fixed several small bugs and typos

v.0.6.2
========
* Q2 residuals renamed to Q (Squared residual distance)
* All plots have parameters `lab.col` and `lab.cex` for changing color and font size for data point labels

v.0.6.1
========
* fixed a bug led to incorrect calculation of specificity
* jack-knife confidence intervals now also calculated for PLS-DA models
* confidence intervals for regression coefficients are shown by default if calculated

v.0.6.0
========
* randomization test for PLS has been added, see `?randtest`
* systematic and repeated random cross-validation are available, see `?crossval` 
* fixed bug with labels on bar plot with confidence intervals
* fixed bug in PLS when using maximum number of components lead to NA values in weights

v. 0.5.3
========
* fixed several small bugs
* improvemed documentation for basic methods

v. 0.5.2
========
* fixed bug for computing classification performance for numeric class names
* improvements to SIMCA implementation

v. 0.5.1
========
* added more details to documentation
* bug fixes for variable selection methods

v. 0.5.0
========
* all documentation has been rewritten using `roxygen2` package
* added extra preprocessing methods
* added VIP scores calculation and plot for PLS and PLS-DA models
* addec Selectivity ratio calculation and plot for PLS and PLS-DA models
* added calculation of confidence intervals for PLS regression coefficient using jack-knife
* bug fixes and small improvements
* the first release available in CRAN

v. 0.4.0
========
* New `classres` class for representation and visualisation of classification results
* in PCA model, limits for T2 and Q2 now are calculated for all available components
* in PCA results, limits for T2 and Q2 calculated for a model are kept and shown on residuals plot 
* added parameters `xticklabels` and `yticklabels` to `mdaplot` and `mdaplotg` functions
* New `simca` and `simcares` classes for one-class SIMCA model and results
* New `simcam` and `simcamres` classes for multiclass SIMCA model and results
* New `plsda`and `plsdares`classes for PLS-DA model and results
* bug fixes and improvements

v. 0.3.2
========
* Enhancements in group bar plot
* Fixed bugs with wrong labels of bar plot with negative values

v. 0.3.1
========
* Corrected errors and typos in README.md and small bg fixes

v. 0.3.0
========
* PLS and all related methods were rewritten from the scratch to make them faster, more efficient
and also to follow the same code conventions as previously rewritten PCA. Here are main changes
you need to do in your code if you used mdatools PLS before: `selectNumComp(model, ncomp)` instead
of `pls.selectncomp(model, ncomp)`, `test.x` ad `test.y` instead of `Xt` and `yt`, finally separate logical
arguments `center` and `scale` are used instead of previously used `autoscale`. By default `scale = F` and `center = T`.
* PLS and all related methods are now well documented (see `?pls`)
* plotting tools for all classes and methods were rewritten completely. Now all plotting methods 
use either `mdaplot` or `mdaplotg` functions, which extend basic functionality of R plots. For example, 
they allow to make color groups and colorbar legend, calculate limits automatically depending on 
elements on a plot, make automatic legend and many other things.
