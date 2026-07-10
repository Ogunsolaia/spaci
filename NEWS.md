# spaci 0.1.0.9000 (development)

* The `"mle"` Matérn recovery engine now **fixes the smoothness at `nu = 0.5`
  (exponential) by default**, controlled by the new `matern_nu` argument of
  `recoverU()` / `recoverUplus()`. The free four-parameter fit is poorly
  identified on weak residual fields and could send the smoothness estimate to a
  numerical boundary; pass `matern_nu = NULL` for the previous behaviour. The
  `"geoR"` engine is unchanged.
* New `bias_bound()`: an estimated post-matching bias bound for an `idaps()` fit
  (covariate, exposure and variogram-based confounding terms), with a
  `print()` method.
* Matching estimators (`idaps()`, `daps()`, `naive_ps()`) gain a
  `match_method` argument: `"greedy"` (default, as before) or `"optimal"`, a
  deterministic 1:1 assignment via `clue::solve_LSAP()` that needs no seed.

# idaps 0.1.0

* First release. Implements the `idaps()` (distance-adjusted propensity score
  with interference) and `recoverUplus()` (doubly robust with recovered spatial
  confounder and neighbourhood exposure) estimators, together with the
  `naive_ps()`, `daps()` and `recoverU()` comparators.
* `simulate_spatial_causal()` generates data with joint spatial confounding and
  interference; `spatial_ate()` runs all estimators and collects the results.
* The recovered-confounder step uses a self-contained Matérn maximum-likelihood
  fit by default (`matern_method = "mle"`), with an optional `geoR` engine for
  faithful reproduction of the report.
