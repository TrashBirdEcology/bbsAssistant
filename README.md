**bbsAssistant**: An R package for downloading and handling data and
[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square)](#contributors)
information from the North American Breeding Bird Survey.
================
Last updated: 2019-11-26

<!-- README.md is generated from README.Rmd. Please edit that file and render to push updates.-->

[![status](https://joss.theoj.org/papers/4b445373a7a7806c92e17bdd194a8e69/status.svg)](https://joss.theoj.org/papers/4b445373a7a7806c92e17bdd194a8e69)[![License:
CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](http://creativecommons.org/publicdomain/zero/1.0/)[![lifecycle](https://img.shields.io/badge/lifecycle-maturing-lightgrey.svg)](https://www.tidyverse.org/lifecycle/#maturing)[![Travis
build
status](https://travis-ci.org/trashbirdecology/bbsAssistant.svg?branch=master)](https://travis-ci.org/trashbirdecology/bbsAssistant)<img src="man/figures/logo.png" align="right" height=140/>

## About

This R package contains functions for downloading and munging data from
the [North American Breeding Bird
Survey](https://www.pwrc.usgs.gov/bbs/) (BBS) [via
FTP](https://www.pwrc.usgs.gov/BBS/RawData/) (Pardieck et al. 2018; J.
R. Sauer et al. 2017). This package was created to allow the user to
bulk-download the BBS point count and related (e.g., route-level
conditions) via FTP, and to quickly subset the data by taxonomic
classifications and/or geographical locations. This package also
maintains data containing the trend and annual indices from the most
recent (1996-2017) [hierarhchical popultion trend
analyses](https://www.mbr-pwrc.usgs.gov/bbs/) (J. Sauer et al. 2017).

## Quick Start

### Installing **bbsAssistant**

Install the development version of this package using devtools and load
the package and dependencies:

``` r
devtools::install_github("trashbirdecology/bbsAssistant", 
                         dependencies = TRUE, 
                         force=TRUE) # force to get most recent dev version
library(bbsAssistant)
```

## Quick-download and import

Quickly retrieve all or a subset (states/regions) of the BBS data using
the wrapper function,
`quick_get_bbs()`:

``` r
bbs<- bbsAssistant::quick_get_bbs(state.names = c("Florida", "Nebraska"),  # get only two states for convenience. Leave blank to retrieve all states/regions.
                     overwrite.bbs = FALSE, overwrite.routes = FALSE,  # overwrite routes.csv and bbs data = FALSE
                     get.conditions = TRUE, overwrite.conditions = FALSE) # get weather conditions, does not overwrite
```

## Additional Information

### Vignettes and package manual

For function descriptions please build the manual
(`devtools::build_manual("bbsAssistant)`) and for an example build the
vignette (`devtools::build_vignettes()`; or run
`/vignettes/vignettes.Rmd`).

### Contributions to and interactions within the project

To make a contribution visit the
[CONTRIBUTIONS.md](https://github.com/trashbirdecology/bbsAssistant/CONTRIBUTING.md).
Contributors **must adhere to the [Code of
Conduct](https://github.com/trashbirdecology/bbsAssistant/CODE_OF_CONDUCT.md).**
For questions, comments, or issues, feel free to email the maintainer
[Jessica Burnett](mailto:jburnett@usgs.gov) or submit an
[Issue](https://github.com/TrashBirdEcology/bbsAssistant/issues)
(preferred).

## Contributors ✨

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore -->
<table>
  <tr>
    <td align="center"><a href="http://trashbirdecology.github.io"><img src="https://avatars2.githubusercontent.com/u/9939381?v=4" width="100px;" alt="Jessica Burnett"/><br /><sub><b>Jessica Burnett</b></sub></a><br /><a href="#userTesting-TrashBirdEcology" title="User Testing">📓</a> <a href="#review-TrashBirdEcology" title="Reviewed Pull Requests">👀</a> <a href="https://github.com/TrashBirdEcology/bbsAssistant/commits?author=TrashBirdEcology" title="Tests">⚠️</a></td>
  </tr>
</table>

<!-- ALL-CONTRIBUTORS-LIST:END -->
Thanks goes to these wonderful people ([emoji
key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->

<!-- prettier-ignore -->

<table>

<tr>

<td align="center">

<a href="http://ethanwhite.org"><img src="https://avatars0.githubusercontent.com/u/744427?v=4" width="100px;" alt="Ethan White"/><br /><sub><b>Ethan
White</b></sub></a><br /><a href="#review-ethanwhite" title="Reviewed Pull Requests">👀</a>

</td>

</tr>

</table>

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the
[all-contributors](https://github.com/all-contributors/all-contributors)
specification. Contributions of any kind welcome\!

## Acknowledgments

We especially thank the participatory scientists who collect data
annually for the North American Breeding Bird Survey, and the Patuxent
Wildlife Research Center for making these data publicly and easily
accessible. We thank those who have made
[contributions](https://github.com/TrashBirdEcology/bbsAssistant/graphs/contributors)
of all sizes to this project. Finally, we thank
(<span class="citeproc-not-found" data-reference-id="ethanwhite">**???**</span>)(www.github.com/ethanwhite)
and
(<span class="citeproc-not-found" data-reference-id="jsta">**???**</span>)(www.github.com/jsta),
whose feedback greatly improved the quality of this software. This
software is preliminary or provisional and is subject to revision. It is
being provided to meet the need for timely best science. The software
has not received final approval by the U.S. Geological Survey (USGS). No
warranty, expressed or implied, is made by the USGS or the U.S.
Government as to the functionality of the software and related material
nor shall the fact of release constitute any such warranty. The software
is provided on the condition that neither the USGS nor the U.S.
Government shall be held liable for any damages resulting from the
authorized or unauthorized use of the software.

## References

<div id="refs" class="references">

<div id="ref-pardieck2018north">

Pardieck, KL, DJ Ziolkowski Jr, M Lutmerding, and MAR Hudson. 2018.
“North American Breeding Bird Survey Dataset 1966–2017, Version
2017.0.” *US Geological Survey, Patuxent Wildlife Research Center,
Laurel, Maryland, USA.\[online\] URL:
Https://Www.pwrc.usgs.gov/BBS/RawData*.

</div>

<div id="ref-sauer2017first">

Sauer, John R, Keith L Pardieck, David J Ziolkowski Jr, Adam C Smith,
Marie-Anne R Hudson, Vicente Rodriguez, Humberto Berlanga, Daniel K
Niven, and William A Link. 2017. “The First 50 Years of the North
American Breeding Bird Survey.” *The Condor: Ornithological
Applications* 119 (3). Oxford University Press: 576–93.
<https://doi.org/10.1650/CONDOR-17-83.1>.

</div>

<div id="ref-sauer2017north">

Sauer, JR, D Niven, J Hines, David Ziolkowski Jr, KL Pardieck, JE
Fallon, and William Link. 2017. “The North American Breeding Bird
Survey, Results and Analysis 1966-2015.”

</div>

</div>
