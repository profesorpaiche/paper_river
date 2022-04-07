# Information

**Heat stress indicators in CMIP6: Estimating future trends and exceedances of
impact-relevant thresholds**

- Authors: Schwingshackl et al.
- Year: 2021
- Journal: Earth's Future
- DOI: https://doi.org/10.1029/2020EF001885
- Tags:
    - [CC] Climate change.
    - [Ext] Extremes.
    - [Heat] Heat related.

# Notes

> Supplementary document has very interesting information.

## Introduction

Many attempts for heat stress indicators (HSIs) had been developed in the past as
a way to express the physiological response of the human health to the
environment. The majority relies on temperature, humidity, and solar and thermal
radiation, and a few considers also wind.

> There is a small list of applications of HSIs.

Epidemiological studies have determine that there is no HSI that is superior to
another, almost all of them have the same level of performance. Some differences
can be found under specific conditions, like small regions or the endpoint of the
indicator (work, sports, urban). Consequently, it is common to find studies that
do not use HSIs, but statistical methods based on temperature and humidity.

On the other hand, climate impact assessments use HSIs because it allows a simple
estimation of the reaction of humans to meteorological variables and have
different applications (sports, construction, work) that can be projected in the
future. Additionally, HSIs are more robust projections of heat stress than just
temperature due to its co-variability with humidity.

## Methods and data

The HSIs used are:

- Daily maximum near-surface air temperature (TX)
- Apparent temperature (AT)
- NOAA Heat Index (HI)
- Humidex (Hu)
- Wet-bulb temperature (Twb)
- Wet-bulb globe temperature (Twbg)
- Simplified wet-bulb globe temperature (Twbgs)
- Universal Thermal Climate Index (UTCI)

"The assessment of HSI trends does not allow for direct derivations of
society-relevant impacts because HSI trends inherently depend on the scales on
which the HSIs are defined. To classify the severity of human heat stress, we
thus employ impact-relevant thresholds". Because the HSIs are defined for
different purposes there is no uniform impact assessment, so a 4 level scale was
created for this study according to different studies.

24 models from the CMIP6 were used. All of them have the data necessary to
calculate the HSIs with some caveats to take in consideration. The calculation
was done over land (grid-cells with at least 50% of land fraction). Population
gridded data is also used since HSIs are related to humans.

HSIs scale linearly with global mean temperature and the interval between the
levels of different HSIs was normalized to allow trends and thresholds
comparisons.

Climate models and projections have some biases. To adjust the bias, quantile
delta mapping (QDM) was used for the correction and then compared to quantile
mapping and multivariate bias correction to check robustness.

## Results

In general, all the HSIs present a faster warming (positive trend) compared to
the global mean temperature (GMT), even though the HSIs are a linear function of
GMT. The behaviour of each one of the HSIs depends on how the analysis is done
(either the absolute value or the normalized according to the threshold
intervals).

Evaluating the number of days HSIs exceed a threshold is more important than
analysing the trend. Under a warming climate there is a clear evidence that the
number of exceedances per year increases dramatically is most of the regions
analyzed. Considering populated areas, only levels 1 and 2 are present today, but
all levels (up to 4) are reached with global warming, especially 2 and 3. The
regions close to the equator (like the Amazon region) are exposed to a higher
increases in the number of exceedances.

## Discussion

Although all the HSIs shows an increase on both trend and frequency of
exceedance, a normalization must be done in order to do the comparison. This
leads to interesting results where high HSI trend do not necessary means a higher
increase in the exceedance. This is something important to keep in mind since
HSIs have different applications (epidemiology, heat alarming systems,
occupational work, among others).

"Acclimatization to heat depends on the geographic region, and using globally
uniform thresholds is thus a strong simplification". Human behavior and other
socio-economic characteristics must be considered as well since those can change
the level of vulnerability of a population. The study did not take in
consideration the ability of humans to adapt to heat stress scenarios, so the
HSIs could be an overestimation in places where insolation and cooling systems
can be used. However, low income countries have poor housing conditions, which
can be consider similar to outdoors, making the HSIs values from this study more
accurate for these regions.

## Conclusions

- There is a high spread in the trends and exceedances frequency among all HSIs,
  so one should choose carefully.

- The study do not recommend any specific HSIs for epidemiological study, which
  goes in line with other studies that concludes there is no superior HSI.

# Bibtex

@article{Schwingshackl_2021,
    author = {Schwingshackl, Clemens and Sillmann, Jana and Vicedo-Cabrera, Ana Maria and Sandstad, Marit and Aunan, Kristin},
    title = {Heat Stress Indicators in CMIP6: Estimating Future Trends and Exceedances of Impact-Relevant Thresholds},
    journal = {Earth's Future},
    volume = {9},
    number = {3},
    pages = {e2020EF001885},
    keywords = {climate change, climate extremes, global climate modeling, heat stress, heat-related health impacts, thermal indices},
    doi = {https://doi.org/10.1029/2020EF001885},
    url = {https://agupubs.onlinelibrary.wiley.com/doi/abs/10.1029/2020EF001885},
    eprint = {https://agupubs.onlinelibrary.wiley.com/doi/pdf/10.1029/2020EF001885},
    note = {e2020EF001885 2020EF001885},
    year = {2021}
}

