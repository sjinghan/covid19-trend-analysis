# Healthcare System Capacity and COVID-19 Mortality Analysis

**Author:** Jinghan Sun  <br>
**Last updated:** May 2, 2025

## Abstract
Modivated by frequent reports of hospital strain during the COVID019 pendemic, this project examines whether countries with more hospital beds experienced lower COVID-19 mortality. Using the Our World in Data (OWID) dataset, I analyzed bed capacity alongside demographics and regional context. **Result:** median age shows a strong positive correlation with mortality ($r = 0.65$). Bed capacity exhibits a non-linear (inverted-U) relationship and substantian within category variance. **Conclusion:** demography dominates; beds alone are incomplete for analyzing system resilience. 

## Key takeaways
- Age structure stands out. Older populations leads to higher mortality. 
- Capacity does not equate to monotonic protection: more beds did not consistently mean fewer deaths; realtionship is non-linear. 
- Regional context is important. Europe/South America, generally higher; Asia/Oceania lower on average. 

## Figures
See ***healthcare_system_capacity_analysis.Rmd*** for all plots and commentary. 

## Methods
- **Outcome:** maximum deaths per million (country-level summary).
- **Predictors:** hospital beds per 1,000 (capacity proxy), median age; continent used for visual grouping. 
- **Visuals:** scatter with LOESS smoother, capacity boxplots, ranked bars, continent $x$ capacity bars. 
- **Note:** This is an exploratory ecological analysis; assoviations are descriptive, not causal. 

## Conclusions
- **Demography dominates:** Median age is the most consistent correlate of mortality ($r = 0.65$). 
- **Capacity is context-dependent:** Bed supply shows a non-linear association and does not reliably predict lower mortality across countries. 
- **Heterogeneity:** Regional differences and outliers highlight the role of timing, policy, vaccination, and reporting practices beyond capacity alone. 

## Limitations
- Country-level (ecological) analysis; not individual-level inference. 
- Peak deaths metric is sensitive to reporting spikes and wave timing. 
- Beds/1,000 is not a optimal proxy; ignores ICU, staffing, surge ability, access and quality. 
- Capacity bins are arbitrary; within-group heterogeneity is large. 
- Demographics, vaccination, policy timing, variants and data quality are not fully adjusted here. 

## Next steps
- Add cumulative/smoothed peak deaths and, wherr available, excess mortality. 
- Fit multivariable models (e.g., linear/GAM) adjusting for median age, vaccination, policy timing/strictness, GDP per capita, urbanization, and regional effects.
- Sensitivity: treat beds ads continuous, vary cutoffs, exclude smaller states, split by variant periods. 
- Report adjusted estimates, and marginal-effect/partial-dependence plots. 

## Data & license
- **Data:** Our World in Data (OWID) COVID-19 dataset. 
- **License:** OWID content is available under **CC BY**; credit OWID and original sources. 
- **How to cite the data (APA):** 
Edouard Mathieu, Hannah Ritchie, Lucas Rodés-Guirao, Cameron Appel, Daniel Gavrilov, Charlie Giattino, Joe Hasell, Bobbie Macdonald, Saloni Dattani, Diana Beltekian, Esteban Ortiz-Ospina, and Max Roser (2020). *COVID-19 Pandemic*. Our World in Data. <https://ourworldindata.org/coronavirus>

## Acknowledgments
Thanks to the OWID team and their upstream sources for maintaining an open, comprehensive dataset that enabled this exploratory work. 
