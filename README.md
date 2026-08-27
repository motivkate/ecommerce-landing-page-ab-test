# E-commerce Landing Page A/B Test Analysis

**Author:** Kateryna Ventskovska
**Role:** Data Science & Analytics  
**Date:** August 2026  

---

## Project overview
This project evaluates an A/B test conducted by an e-commerce company to test a redesigned landing page against its existing version.

The primary objective is to determine whether rolling out the new landing page drives a statistically significant increase in the conversion rate. The overall evaluation criterion is the user conversion rate, defined as unique converted users divided by total unique users.

The experiment tests the null hypothesis that the new page conversion rate is less than or equal to the old page conversion rate, against the alternative hypothesis that the new page produces a higher conversion rate, evaluated at a 5% significance level ($\alpha = 0.05$).

The dataset includes 294,478 log entries recorded in January 2017 across three markets (United States, United Kingdom, and Canada), tracking user identifiers, timestamps, assigned experiment groups, landing page variants, and binary conversion outcomes.

---

## Executive summary
The A/B test conducted across 290,584 users demonstrated that the new landing page did not generate an uplift in conversion rate compared to the existing design.

* **Control page conversion rate:** 12.04% (17,489 / 145,274)
* **Treatment page conversion rate:** 11.88% (17,264 / 145,310)
* **Absolute lift:** -0.16%
* **Relative change:** -1.33%
* **Statistical significance:** with a $p$-value of ~0.19 and a 95% Confidence Interval of `[-0.39%, +0.08%]`, the result is not statistically significant at the $\alpha = 0.05$ level.
* **Geographic breakdown:** the lack of conversion uplift is consistent across all three analyzed markets (US, UK, CA).

---

## Final business recommendation
**Keep the existing page** and **test a more substantially different page**.
* **Financial risk:** launching the new variant projects an estimated loss of ~160 conversions per 100k visitors with zero return on design and engineering investments.
* **Next steps:** conduct qualitative user research (heatmaps, UX surveys) and iterate with stronger value-proposition changes rather than minor visual redesigns.

---

## Tech Stack & Methodology
* **Python libraries:** `pandas`, `numpy`, `scipy`, `statsmodels`, `matplotlib`, `seaborn`
* **Statistical methods:** Two-Proportion Z-Test, Chi-Square Test of Independence, Permutation Test (1,000 iterations), Bootstrap Analysis (95% CI).

---

## Dataset source
* Based on the repository [`Udacity-DAND-AB-test-ecommerce`](https://github.com/jemc36/Udacity-DAND-AB-test-ecommerce) by `jemc36`.
* Task guidelines and roadmap followed educational materials by **Berkhan** (Instagram: [@pirknn](https://instagram.com/pirknn)).
* Data cleaning, statistical modeling, visualizations, and business conclusions were independently developed by the author.


