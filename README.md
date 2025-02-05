# Breast Cancer Cohort Analysis

## Overview

This project aims to analyze the survival outcomes of breast cancer patients who transitioned between different treatment regimens. Two cohorts are compared based on their treatment paths:

- **Cohort 1**: Patients transitioning from FEC (Fluorouracil, Epirubicin, Cyclophosphamide) to DOCETAXEL.
- **Cohort 2**: Patients transitioning from CYCLOPHOSPHAMIDE + EPIRUBICIN + FLUOROURACIL to TRASTUZUMAB.

The goal of the analysis is to determine if the treatment transitions affect patient survival, using a synthetic dataset representing breast cancer patients.

## Contents

- **Introduction**: A summary of the analysis objectives and dataset.
- **Methodology**: Detailed steps for data exploration, cohort creation, and statistical analysis.
- **Results**: Statistical test results comparing survival between the two cohorts.
- **Discussion and Conclusion**: Interpretation of findings, justifications for analysis choices, and limitations of the study.
- **Recommendations for Future Work**: Suggestions for enhancing the analysis.

## Dataset

The dataset used in this analysis consists of three key tables:

1. **Patients**: Demographic and clinical details of each patient.
2. **Diagnosis**: Includes tumor stage, grade, and diagnosis dates.
3. **Treatment**: Details of treatment regimens, start and end dates.

The data used is synthetic and created for the purpose of this cohort analysis.

## Methodology

1. **Data Preprocessing**:
    - Missing values in key columns (e.g., height, weight) were imputed using the mean.
    - Survival months were calculated by taking the difference between diagnosis and death dates and rounding to the nearest whole month.

2. **Cohort Creation**:
    - Two cohorts were created based on the most common treatment transitions observed in the dataset.
    - Cohort 1: FEC → DOCETAXEL
    - Cohort 2: CYCLOPHOSPHAMIDE + EPIRUBICIN + FLUOROURACIL → TRASTUZUMAB
    - The cohorts were balanced based on age, gender, and tumor stage to minimize confounding factors.

3. **Survival Analysis**:
    - Survival months were calculated and compared using a t-test to determine if there was a statistically significant difference between the cohorts.
    - The t-test was chosen based on the assumption that the data followed a normal distribution and that variances were equal across groups.

## Results

- **Descriptive Statistics**: 
    - Cohort 1: Mean survival = 24 months (SD = 5.5).
    - Cohort 2: Mean survival = 23.5 months (SD = 6.0).
  
- **Statistical Test**: 
    - The t-test revealed no significant difference in survival months between Cohort 1 and Cohort 2 (p > 0.05).

- **Visualizations**:
    - Survival distributions for both cohorts were plotted, though missing data impacted some visualizations.

## Discussion

The analysis found no statistically significant difference in survival between the two cohorts based on the synthetic data. This suggests that, within the context of this dataset, the transition between FEC → DOCETAXEL and CYCLOPHOSPHAMIDE + EPIRUBICIN + FLUOROURACIL → TRASTUZUMAB does not significantly influence survival. However, further research with real-world data may yield different findings.

### Justifications

- **Cohort Selection**: Chosen based on the most common treatment transitions, ensuring a real-world relevant analysis.
- **Statistical Test**: The t-test was appropriate given the normality of the data and equal variances assumption.

### Limitations

- **Data Quality**: Missing or incomplete data limited the analysis, particularly in visualizations.
- **Synthetic Data**: The findings are based on synthetic data and may not reflect real-world outcomes.
- **Confounding Factors**: Variables like patient comorbidities and treatment adherence were not considered, which could affect survival.

### Recommendations

- Use more comprehensive, real-world data to validate the findings.
- Include additional variables such as treatment response, comorbidities, and adherence to improve the model's accuracy.
- Consider advanced survival analysis techniques like Cox regression to account for multiple factors.

## Conclusion

This cohort analysis provides insights into breast cancer treatment transitions and their impact on survival. However, due to the synthetic nature of the dataset, further investigation with real patient data is recommended to confirm these results.

## License

This project is for educational and assessment purposes only. The synthetic dataset and findings should not be interpreted as reflecting real-world clinical data.
