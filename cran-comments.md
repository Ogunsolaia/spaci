## Test environments

* Windows 11 x64
* R 4.6.0

## R CMD check results

R CMD check was run with `--as-cran` and returned:

* 0 errors
* 0 warnings
* 3 notes

### Notes

* This is a new submission.

* One example (`spatial_ate()`) takes slightly longer than 5 seconds to run on my machine (approximately 6 seconds). I reduced the example as much as possible while keeping it useful for illustrating the method.

* The note about the V8 package arises from the local checking environment and does not affect the package functionality.

## Package summary

`spaci` provides methods for causal effect estimation from spatial observational data in the presence of spatial confounding and spatial interference. The package implements the iDAPS and recoverU+ methods, together with comparator approaches and simulation tools for methodological evaluation.

Thank you for your time and consideration.
