# Information

**Case-crossover analyses of air pollution exposure data**

- Authors: Janes, Sheppard & Lumley.
- Year: 2005.
- Journal: Epidemiology. Vol. 16, Num. 6
- DOI: ?
- Tags:
    - [CxO] Case-crossover.

# Notes

## Introduction - Explanation of case-crossover study

Case-crossover design is an approach for studying effects of day-to-day variation
in pollution on morbidity or mortality. For this situation, the exposure is the
ambient air pollution concentration. This exposure is used for all subjects in
the study and hence is called a "shared" exposure series.

Confounding is something that should be consider when we deal with effects of
weather or environment. Confounding could be time-independent even with shared
exposure series or time-dependent with seasons or other pollutants. The later can
be troublesome since biases are frequently found.

Case-crossover design can solve both of the issues mentioned, where a sample of
subjects' exposure just before an event is compared with exposure a comparable
control. By design, time-independent confounders are controlled since comparison
are made within the same subject. Time-dependent confounders are controlled by
matching in time the referent window with the time-scale of the confounders (for
example, referents are restricted to the same season as the case group). This
makes the selection of time referents important to control the time-dependent
confounders.

Case-crossover design makes the assumption that there is no trend within the time
window selected.

## The case-crossover method

Appropriate for assessing the association between rare short-term exposure and
the risk of an acute event.

_They explain a little about "condition on exposure" but is not clear to me._

Ambient air pollution exposure is exogenous or generated independently of the
individual under study.

Case-crossover has several strengths:

- Does not require a control sample.
- Effect modification assessment relatively simple.
- Control of time-independent confounders by design.
- Control of time-dependent confounders by matching.

Compared to time-series regression, case-crossover does not require the modeling
of confounders, but it can be included for further control.

Case-crossover design requires that there be no time trend in the exposure within
the referent window. If, for example, referents are always before the case window
and there is a decreasing trend in the exposure, the effect estimate will be
negative biased.

## Referent schemes

The referent schemes is all about the methodology to pick the referent times
(case and control time windows). These schemes can be classify as localizable or
nonlocalizable and ignorable or nonignorable. Localizable is desired because
allows the control of effects from time-dependent confounders. For ignorable
designs, the referent sampling scheme can be ignored. Conditional logistic
regression yields unbiased estimates for localizable ignorable designs.

Types of referent schemes:

- Unidirectional: For air pollution, it can lead to time trend bias.
- Full-Stratum bidirectional: Not good for death analysis. Also, time-dependent
  confounding must be controlled by modeling.
- Symmetric bidirectional: Solves some issues from before but it is
  nonlocalizable.
- Time-stratified: _Seems to be quite good._
- Semi-symmetric bidirectional: Referents are randomly selected from fixed lags.

## Overlap bias

Although it suggests that designs with referent windows is overlapping is subject
to overlap bias whereas designs with disjoint windows are not, this is not the
case. It refers more to a mathematical situation and it depends on the data and
confounders.

Case-crossover involves a trade-off between bias and efficiency. Increasing the
numner of referents will improve efficiency but decreases the control over
confounding, hence increasing possible bias. Positive autocorrelation is the
exposure series also decreases efficiency because there is a relationship in the
exposure between the referent windows. It is advisable to choose referents that
are not adjacent to the index time.

## Case-crossover methods for unshared exposure series

The unshared exposures where each subject experience and individual exposure, we
can consider this situation as if the exposure comes from a random distribution.
However, not all unshared exposures are random. In the situation of exposures
from different regions but spatially correlated, one cannot say that the
exposures are random, but neither shared. It would depend on each case how to
consider the relationship between the exposure and many subjects.

## Discussion and conclusions

It is important to check for time-dependent confounding, time trends and
autocorrelation in the exposure series. Referents should match on the dominant
confounder and should be sampled bidirectionally. If possible, larger number of
referents is recommended to increase the efficiency.

The authors recommend the use of time-stratified referent selection, because it
avoids overlap and trend bias. Stratifying on year and month is adequate for most
studies, but other variables should be consider as well.

# Bibtex

@article{Janes_2005,
    ISSN = {10443983},
    URL = {http://www.jstor.org/stable/20486135},
    author = {Holly Janes and Lianne Sheppard and Thomas Lumley},
    journal = {Epidemiology},
    number = {6},
    pages = {717--726},
    publisher = {Lippincott Williams & Wilkins},
    title = {Case-Crossover Analyses of Air Pollution Exposure Data: Referent Selection Strategies and Their Implications for Bias},
    volume = {16},
    year = {2005}
}

