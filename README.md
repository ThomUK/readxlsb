# readxlsb
Import 'Excel' binary (.xlsb) workbooks into R

[![build](https://github.com/ThomUK/readxlsb/actions/workflows/build.yml/badge.svg)](https://github.com/ThomUK/readxlsb/actions/workflows/build.yml)

```r
library(readxlsb)
read_xlsb(path = system.file("extdata", "TestBook.xlsb", package="readxlsb"), range="PORTFOLIO")
```

## Installation

### Prebuilt binary (no Rtools or Xcode needed)

Prebuilt Windows and macOS binaries for R 4.4, 4.5 and 4.6 are attached to each
[GitHub Release](https://github.com/ThomUK/readxlsb/releases). Pick the file
matching your operating system and R version (check with `R.version.string`),
then install it directly. For example, on Windows with R 4.5:

```r
install.packages("Rcpp")  # runtime dependencies
install.packages(c("xml2", "cellranger"))
install.packages(
  "https://github.com/ThomUK/readxlsb/releases/latest/download/readxlsb_0.1.61_R4.5_windows.zip",
  repos = NULL, type = "win.binary"
)
```

On macOS use the matching `.tgz` file and `type = "mac.binary"`.

Binaries from every commit are also available as artifacts on the
[Actions tab](https://github.com/ThomUK/readxlsb/actions).

### From source

Requires a C++17 compiler (Rtools on Windows, Xcode command line tools on macOS).

```r
# install.packages("remotes")
remotes::install_github("ThomUK/readxlsb")
```
