# Information

**Construction of a high-resolution gridded rainfall dataset for Peru from 19811
to the present day**

- Authors: Aybar, Fernández, Huerta, Lavado Vega & Felipe-Obando
- Year: 2020
- Journal: Hydrological Sciences Journal
- DOI: 10.1080/02626667.2019.1649411
- Tags:
    - [Pe] Peru.
    - [Grid] Gridded data.
    - [ResUp] Improving resolution.

# Notes

## Introduction

Although weather stations are good to understand the water cycle and its impact
on natural and human systems; strong spatial variability, sparse distributions of
rain gauges, and serious data quality issues limits its use in Peru.

Gridded data from satellites and re-analysis can be used, but they also come with
deficiencies like huge errors in the Andean Mountains, overestimation in the
western side of the country, and coarse resolution.

There are some products that combine gridded data with weather stations, but one
must be careful of its performance because the validation process could have use
the same weather stations used in the blended product, just to mention and
example.

Some considerations when creating this blended products:

- Geostatistics methods perform well for annual and monthly products, for daily
  one can also use deterministic methods.
- Gap-filling is very important.
- Simple ratios based on very high rainfall climatologies decreases bias.

## Methods and Data

The study area was divided in 5 regions base on the classification of Manz et al
(2017): the Pacific coast, the western and eastern Andean slopes, the
Andes-Amazon transition, and the Amazon lowlands.

A three-step quality control was used, though it is consider quite conservative due to several limitations, so some data error may remain in the data:

- General problems: Delete obvious inconsistent values.
- Spatial extreme values: Delete all the daily records that exceed a 200 years
  return period threshold, unless the event is found in neighbouring stations.
- Break and bad segments: Manual look for inhomogeneities.

For the gap-infilling the CUTOFF method was applied. In case the conditions for
CUTOFF were not met (< 100 km distance, 10 years of shared data and daily/monthly
correlation > 0.5/0.8) the quantile mapping bias correction was used.

The blended product uses CHIRPM gridded data.

> There is more to say in the creation of the product, but it is too technical to
be included here

## Results and discussions

Around 50% of the rain gauges where discarded, being the missing data the main
reason for the discarded stations. This makes the network just acceptable for the
study.

> I have my doubts about the data quality but there is no much we can de about
it.

The infilling methods filled 44% of monthly data and 58% of daily data.
Mann-Kendall and Kolmogorov-Smirnov statistical tests were used to determine
whether the performance of the gap-infilling procedure is appropriate.

> This amounts are very high. Basically the PISCO product might have been created
from 50% "artificial" observations.

In general, PISCO products have better performance compared to CHIRPS, but the
gridded products are not sufficiently accurate for capturing heavy rainfall
events.

> Although PISCO is better than CHIRPS, it does not mean that PISCO is a good
product since it has major flaws as well.

## Conclusions

- "The gaps in rainfall time series represent the most determining problem for
  the construction of a temporally consistent gridded product".
- PISCO is more suitable for representing area rainfall, except for the Amazon
  lowland where CHIRPM works better.
- Daily PISCO is not able to detect convective storms.

# Bibtex

@article{doi:10.1080/02626667.2019.1649411,
    author = {Cesar Aybar and Carlos Fernández and Adrian Huerta and Waldo Lavado and Fiorella Vega and Oscar Felipe-Obando},
    title = {Construction of a high-resolution gridded rainfall dataset for Peru from 1981 to the present day},
    journal = {Hydrological Sciences Journal},
    volume = {65},
    number = {5},
    pages = {770-785},
    year  = {2020},
    publisher = {Taylor & Francis},
    doi = {10.1080/02626667.2019.1649411},
    URL = {https://doi.org/10.1080/02626667.2019.1649411},
    eprint = {https://doi.org/10.1080/02626667.2019.1649411}
}


