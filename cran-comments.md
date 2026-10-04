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
* Thomas House has been removed from the author list.

<!-- TODO before submitting: CRAN may ask about the removed author. Confirm
     Thomas House agrees, say so in the bullet above, and delete this comment. -->

## Test environments

* Ubuntu Linux x86_64, R 4.5.2 (local)

<!-- TODO before submitting: add the maintainer's own results here
     (e.g. Windows, win-builder R-devel) and delete this comment. -->

## R CMD check results

R CMD check was run with `--as-cran` and returned:

* 0 errors
* 0 warnings
* 0 notes

## Reverse dependencies

There are no reverse dependencies.
