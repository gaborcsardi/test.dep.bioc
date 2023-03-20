
<!-- README.md is generated from README.Rmd. Please edit that file -->

# test.dep.bioc

The goal of **test.dep.bioc** is to test installation of Bioconductor
dependencies with GitHub Actions.

**No Remotes field**

- Pass GitHub Actions.

- Can’t be installed with `install_github()`:

<!-- -->

    dependency ‘limma’ is not available for package ‘test.dep.bioc’

**Remotes with bioc::release/limma**

- GitHub Action failed:

<!-- -->

    Error: 
      ! error in pak subprocess
      Caused by error: 
      ! Could not solve package dependencies:
      * deps::.: ! pkgdepends resolution error for deps::..
      Caused by error: 
      ! Cannot determine package name for 1 package: "bioc::release/limma".
      ℹ Maybe you need to add a `<packagename>=` prefix?

- Can be installed with `install_github()`.
