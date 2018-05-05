# infer 0.2.0.9000
- Filled the `type` argument automatically in `generate()` based
on `specify()` and `hypothesize()`
  - Added message if `type` is given differently than expected
- Implemented `specify() %>% calculate()` for getting observed
statistics.
  - `visualize()` works with either a 1x1 data frame or a vector
    for its `obs_stat` argument
- Refactored `calculate()` into smaller functions to reduce complexity
- Produced error if `mu` is given in `hypothesize()` but `stat = "median"`
is provided in `calculate()` and other similar mis-specifications
- Tweaked `chisq_stat()` to match with `specify() %>% calculate()` framework

# infer 0.2.0

- Switched to `!!` instead of `UQ()` since `UQ()` is deprecated in 
{rlang} 0.2.0
- Added many new files: `CONDUCT.md`, `CONTRIBUTING.md`, and `TO-DO.md`
- Updated README file with more development information
- Added wrapper functions `t_test()` and `chisq_test()` that use a
formula interface and provide an intuitive wrapper to `t.test()` and
`chisq.test()`
- Created `stat = "z"` and `stat = "t"` options
- Added many new arguments to `visualize()` to prescribe colors to shade and 
use for observed statistics and theoretical density curves
- Added check so that a bar graph created with `visualize()` if number of 
unique values for generated statistics is small
- Added shading for `method = "theoretical"` 
- Implemented shading for simulation methods w/o a traditional distribution
  - Use percentiles to determine two-tailed shading
- Changed `method = "randomization"` to `method = "simulation"`
- Added warning when theoretical distribution is used that 
  assumptions should be checked  
- Added theoretical distributions to `visualize()` alone and as overlay with
current implementations being
    - Two sample t
    - ANOVA F
    - One proportion z
    - Two proportion z
    - Chi-square test of independence
    - Chi-square Goodness of Fit test
    - Standardized slope (t)
    
# infer 0.1.1
- Added additional tests
- Added `order` argument in `calculate()`
- Fixed bugs post-CRAN release
- Automated travis build of pkgdown to gh-pages branch

# infer 0.1.0
- Altered the way that successes are indicated in an infer pipeline. 
They now live in `specify()`.
- Updated documentation with examples
- Created `pkgdown` site materials
  - Deployed to https://infer.netlify.com


# infer 0.0.1
- Implemented the "intro stats" examples for randomization methods