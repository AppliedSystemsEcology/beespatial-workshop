[Workshop Website](https://appliedsystemsecology.github.io/beespatial-workshop/)

### Install/Load Packages
If there are issues recreating the environment with `renv` all required packages can be installed by running the following code chunk.

```
load_pkgs <- function(pkgs) {
  inst_pkgs <- pkgs[!pkgs %in% installed.packages()]
  for(p in inst_pkgs) install.packages(p)
  sapply(pkgs,require,character=TRUE)
}

pkgs <- c("terra", "rlandfire", "rgbif",
          "dplyr", "predicts", "tidymodels",
          "sf", "ggplot2", "themis", "pROC",
          "ecospat")
load_pkgs(pkgs)
```
