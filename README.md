[Workshop Website](https://appliedsystemsecology.github.io/beespatial-workshop/)

### Download workshop code from GitHub

To follow along with the workshop on your own computer, you will need to download the contents of this repository, click on the green **\<\>Code** button and select **Download ZIP**. Unzip the downloaded zip file and save the folder to your computer.

```{=html}
<img src="media/downloadcode.png?raw=true"
style="width:50.0%" />
```

### Install/Load Packages

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
