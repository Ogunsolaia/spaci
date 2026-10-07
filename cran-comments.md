## Submission

This is an update of spaci from 0.1.1 to 0.2.0.

## What has changed

* New functions for inference under spatial dependence: `vcov_hac()`,
  `boot_spatial()` and `rand_test()`.
* New `bias_bound()` for `idaps()` fits.
* New `match_method` argument for the matching estimators; `"optimal"` uses
  `clue::solve_LSAP()`. `clue` is in Suggests and is only needed for that option.
* The default Matérn recovery engine now fixes the smoothness at 0.5
  (`matern_nu`), which avoids boundary estimates on weak residual fields.

## Test environments

* Windows 11, R 4.6.0
* Local R CMD check --as-cran


## R CMD check results

R CMD check was run with `--as-cran` and returned:

* 0 errors
* 0 warnings
* 0 notes

## Reverse dependencies

There are no reverse dependencies.
