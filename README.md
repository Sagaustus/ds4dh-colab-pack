<!-- BEGIN GENERATED -->
# DS4DH Practice Pack

Practice notebooks for **Data Science Applied to Housing and Migration Data**
(CourseHub: `dh-and-data-science`), one per technique taught in the course.

## Using them

Each notebook is self-contained — open any one without having run the others.

**In Google Colab:** click the badge at the top of a notebook, then run the
first cell. It will ask you to upload the CSVs; pick them from this pack's
`data/` folder. The upload is remembered for the rest of the session.

**Locally:** put the notebook in the same folder as the CSVs and run it.
Needs `pandas`, `numpy`, `matplotlib`, `scipy`, `scikit-learn`, `statsmodels`.

**Inside CourseHub:** every notebook is also the 📓 Lab Notebook tab on its
lesson, next to the quiz. Nothing to install and no upload step.

## Data

Real Canadian Census shelter-cost data for 194 geographies across four CMAs —
Montréal, Toronto, Edmonton, Vancouver. STIR is the shelter-cost-to-income
ratio, split by immigrant status and owner/renter tenure. These are aggregate
published figures for municipalities and contain no individual-level data.
One unused internal working column has been dropped from `merged_dataset.csv`
in this distributed copy; no notebook reads it.

| File | What it is |
|---|---|
| `merged_dataset.csv` | the main table: 194 geographies x 3 immigrant-status groups (582 rows) |
| `city_summary.csv` | pre-computed CMA-level averages (12 rows) |
| `full_accessibility_index.csv` | published accessibility index per CSD (132 rows) |
| `top10_immigrant_penalty.csv` | published top-10 immigrant renter premium (10 rows) |

## The notebooks

| # | Notebook | Technique |
|---|---|---|
| | **Module 00 — Introduction to DH and Data Science** | |
| `00` | [A First Look at the Housing Data](notebooks/00_first_look.ipynb) | Loading and inspecting a dataset with pandas |
| | **Module 01 — Framing the Right Question** | |
| `01a` | [Descriptive, Analytical and Policy Questions](notebooks/01a_question_typology.ipynb) | Question typology — matching a question to the method that can answer it |
| `01b` | [Reading Data for What Is Missing](notebooks/01b_absence_audit.ipynb) | Absence audit — missing variables, missing populations, missing granularity |
| | **Module 02 — Describing and Comparing Data** | |
| `02a` | [Descriptive Statistics](notebooks/02a_descriptive_stats.ipynb) | Mean, median, standard deviation, IQR — and when each misleads |
| `02b` | [Distributions and Shape](notebooks/02b_distributions_shape.ipynb) | Histograms, skewness, and why shape decides the summary statistic |
| `02c` | [Comparing Groups](notebooks/02c_group_comparison.ipynb) | Group means, absolute gaps, and reversal across levels of aggregation |
| `02d` | [The Immigrant Renter Penalty](notebooks/02d_immigrant_penalty.ipynb) | Ranking responsibly, and converting percentage points into dollars |
| | **Module 03 — Integrating Multiple Data Sources** | |
| `03a` | [Join Keys and Row Explosions](notebooks/03a_join_keys.ipynb) | Merges, composite keys, and detecting one-to-many joins before they corrupt a count |
| `03b` | [Missingness After Merging](notebooks/03b_missingness_after_merge.ipynb) | Structural vs join-induced missingness, and conservation checks |
| | **Module 04 — Statistical Inference** | |
| `04a` | [The t-Test](notebooks/04a_t_test.ipynb) | One-sample t-test on paired within-CSD differences |
| `04b` | [Multiple Comparisons and the Bonferroni Correction](notebooks/04b_bonferroni.ipynb) | Family-wise error rate and the Bonferroni correction |
| `04c` | [Effect Size — Cohen's d](notebooks/04c_cohens_d.ipynb) | Standardised effect size, and why significance and magnitude are different questions |
| | **Module 05 — Regression Analysis** | |
| `05a` | [Ordinary Least Squares](notebooks/05a_ols.ipynb) | OLS, and the fact that a single-dummy regression is a group-mean difference |
| `05b` | [City Fixed Effects](notebooks/05b_fixed_effects.ipynb) | Dummy variables, the dummy trap, and controlling for city without estimating its cost |
| `05c` | [Heteroskedasticity and Robust Standard Errors](notebooks/05c_robust_se.ipynb) | Detecting non-constant residual variance and refitting with HC1 |
| | **Module 06 — Clustering and Segmentation** | |
| `06a` | [Feature Scaling](notebooks/06a_feature_scaling.ipynb) | StandardScaler, and why distance-based methods need it |
| `06b` | [K-Means, the Elbow and the Silhouette](notebooks/06b_kmeans.ipynb) | K-Means clustering and choosing k |
| `06c` | [Ward Hierarchical Clustering](notebooks/06c_ward_hierarchical.ipynb) | Ward linkage, dendrograms, and cross-algorithm agreement as validation |
| | **Module 07 — Machine Learning and Interpretability** | |
| `07a` | [Train/Test Split and Overfitting](notebooks/07a_train_test_split.ipynb) | Holding out data, and why a model's score on its own training data is meaningless |
| `07b` | [Gradient Boosting](notebooks/07b_gradient_boosting.ipynb) | Gradient boosted trees, and the trade of interpretability for accuracy |
| `07c` | [Permutation Importance](notebooks/07c_permutation_importance.ipynb) | Shuffling a feature to measure what the model actually relies on |
| | **Module 08 — Index and Metric Design** | |
| `08a` | [Min-Max vs Z-Score Normalisation](notebooks/08a_normalization.ipynb) | Making units disappear, and inverting polarity so high always means the same thing |
| `08b` | [Building a Composite Index — HAI and XSTIR](notebooks/08b_composite_index.ipynb) | Constructing a number that does not exist in the data |
| `08c` | [Weighting and Rank Sensitivity](notebooks/08c_weighting_sensitivity.ipynb) | Treating weights as a value judgement and testing how much they matter |
| | **Module 09 — Geospatial Analysis** | |
| `09a` | [Spatial Reasoning Without a Map](notebooks/09a_ranking_grouping.ipynb) | Ranking and grouping by geography when you have no boundary files |
| `09b` | [The Modifiable Areal Unit Problem](notebooks/09b_maup.ipynb) | How the choice of spatial unit and weighting changes the answer |
| `09c` | [Measuring Spatial Inequality](notebooks/09c_spatial_inequality.ipynb) | Coefficient of variation vs standard deviation for comparing dispersion |
| | **Module 10 — Data Visualization and Communication** | |
| `10a` | [KDE and Density Estimation](notebooks/10a_kde.ipynb) | Kernel density estimation, bandwidth choice, and boundary artefacts |
| `10b` | [Ranked Bars, Annotation and Encoding](notebooks/10b_ranked_bars.ipynb) | Encoding choices as argument — what a chart claims before anyone reads it |
| `10c` | [Small Multiples](notebooks/10c_small_multiples.ipynb) | Repeated panels, the shared-axis rule, and reference lines |
| | **Module 11 — Policy and Domain Reasoning** | |
| `11a` | [The 'So What?' Test](notebooks/11a_evidence_classification.ipynb) | Classifying findings by what they license — action, monitoring, or context only |
| `11b` | [From Coefficient to Recommendation](notebooks/11b_coefficient_to_policy.ipynb) | Reading a confidence interval as a policy constraint |
| | **Module 12 — Advanced Synthesis** | |
| `12` | [Capstone — Choosing the Right Tool and Stating Honest Limits](notebooks/12_synthesis_capstone.ipynb) | Method selection and writing the scope of valid inference |

## Rebuilding

Notebooks are generated from `colab_pack/` in the coursehub repo.
Edit the content modules there, not the `.ipynb` files:

```bash
python colab_pack/build_pack.py --pack ds4dh --check --zip
```

Every notebook is executed end to end as part of the build, so the worked
answers are known to reproduce the figures quoted in the course.

<!-- END GENERATED -->

# DS4DH Practice Pack

Practice notebooks for **Data Science Applied to Housing and Migration Data**
(CourseHub: `dh-and-data-science`), one per technique taught in the course.

## Using them

Each notebook is self-contained — open any one without having run the others.

**In Google Colab:** click the badge at the top of a notebook, then run the first
cell. It will ask you to upload the CSVs; pick them from this pack's `data/`
folder. The upload is remembered for the rest of the session.

**Locally:** put the notebook in the same folder as the four CSVs and run it.
Needs `pandas`, `numpy`, `matplotlib`, `scipy`, `scikit-learn`, `statsmodels`.

**Inside CourseHub:** every notebook is also the 📓 Lab Notebook tab on its
lesson, next to the quiz. Nothing to install and no upload step.

## Data

Real Canadian Census shelter-cost data for 194 geographies across four CMAs —
Montréal, Toronto, Edmonton, Vancouver. STIR is the shelter-cost-to-income
ratio, split by immigrant status and owner/renter tenure.

| File | Rows | What it is |
|---|---|---|
| `merged_dataset.csv` | 582 | the main table: 194 geographies x 3 immigrant-status groups |
| `city_summary.csv` | 12 | pre-computed CMA-level averages |
| `full_accessibility_index.csv` | 132 | published accessibility index per CSD |
| `top10_immigrant_penalty.csv` | 10 | published top-10 immigrant renter premium |

These are aggregate published census figures for municipalities. They contain no
individual-level data. One unused internal working column has been dropped from
`merged_dataset.csv` in this distributed copy; no notebook reads it.

## The notebooks

| # | Notebook | Technique |
|---|---|---|
| | **Module 00 — Introduction to DH and Data Science** | |
| `00` | [A First Look at the Housing Data](notebooks/00_first_look.ipynb) | Loading and inspecting a dataset with pandas |
| | **Module 01 — Framing the Right Question** | |
| `01a` | [Descriptive, Analytical and Policy Questions](notebooks/01a_question_typology.ipynb) | Question typology — matching a question to the method that can answer it |
| `01b` | [Reading Data for What Is Missing](notebooks/01b_absence_audit.ipynb) | Absence audit — missing variables, missing populations, missing granularity |
| | **Module 02 — Describing and Comparing Data** | |
| `02a` | [Descriptive Statistics](notebooks/02a_descriptive_stats.ipynb) | Mean, median, standard deviation, IQR — and when each misleads |
| `02b` | [Distributions and Shape](notebooks/02b_distributions_shape.ipynb) | Histograms, skewness, and why shape decides the summary statistic |
| `02c` | [Comparing Groups](notebooks/02c_group_comparison.ipynb) | Group means, absolute gaps, and reversal across levels of aggregation |
| `02d` | [The Immigrant Renter Penalty](notebooks/02d_immigrant_penalty.ipynb) | Ranking responsibly, and converting percentage points into dollars |
| | **Module 03 — Integrating Multiple Data Sources** | |
| `03a` | [Join Keys and Row Explosions](notebooks/03a_join_keys.ipynb) | Merges, composite keys, and detecting one-to-many joins before they corrupt a count |
| `03b` | [Missingness After Merging](notebooks/03b_missingness_after_merge.ipynb) | Structural vs join-induced missingness, and conservation checks |
| | **Module 04 — Statistical Inference** | |
| `04a` | [The t-Test](notebooks/04a_t_test.ipynb) | One-sample t-test on paired within-CSD differences |
| `04b` | [Multiple Comparisons and the Bonferroni Correction](notebooks/04b_bonferroni.ipynb) | Family-wise error rate and the Bonferroni correction |
| `04c` | [Effect Size — Cohen's d](notebooks/04c_cohens_d.ipynb) | Standardised effect size, and why significance and magnitude are different questions |
| | **Module 05 — Regression Analysis** | |
| `05a` | [Ordinary Least Squares](notebooks/05a_ols.ipynb) | OLS, and the fact that a single-dummy regression is a group-mean difference |
| `05b` | [City Fixed Effects](notebooks/05b_fixed_effects.ipynb) | Dummy variables, the dummy trap, and controlling for city without estimating its cost |
| `05c` | [Heteroskedasticity and Robust Standard Errors](notebooks/05c_robust_se.ipynb) | Detecting non-constant residual variance and refitting with HC1 |
| | **Module 06 — Clustering and Segmentation** | |
| `06a` | [Feature Scaling](notebooks/06a_feature_scaling.ipynb) | StandardScaler, and why distance-based methods need it |
| `06b` | [K-Means, the Elbow and the Silhouette](notebooks/06b_kmeans.ipynb) | K-Means clustering and choosing k |
| `06c` | [Ward Hierarchical Clustering](notebooks/06c_ward_hierarchical.ipynb) | Ward linkage, dendrograms, and cross-algorithm agreement as validation |
| | **Module 07 — Machine Learning and Interpretability** | |
| `07a` | [Train/Test Split and Overfitting](notebooks/07a_train_test_split.ipynb) | Holding out data, and why a model's score on its own training data is meaningless |
| `07b` | [Gradient Boosting](notebooks/07b_gradient_boosting.ipynb) | Gradient boosted trees, and the trade of interpretability for accuracy |
| `07c` | [Permutation Importance](notebooks/07c_permutation_importance.ipynb) | Shuffling a feature to measure what the model actually relies on |
| | **Module 08 — Index and Metric Design** | |
| `08a` | [Min-Max vs Z-Score Normalisation](notebooks/08a_normalization.ipynb) | Making units disappear, and inverting polarity so high always means the same thing |
| `08b` | [Building a Composite Index — HAI and XSTIR](notebooks/08b_composite_index.ipynb) | Constructing a number that does not exist in the data |
| `08c` | [Weighting and Rank Sensitivity](notebooks/08c_weighting_sensitivity.ipynb) | Treating weights as a value judgement and testing how much they matter |
| | **Module 09 — Geospatial Analysis** | |
| `09a` | [Spatial Reasoning Without a Map](notebooks/09a_ranking_grouping.ipynb) | Ranking and grouping by geography when you have no boundary files |
| `09b` | [The Modifiable Areal Unit Problem](notebooks/09b_maup.ipynb) | How the choice of spatial unit and weighting changes the answer |
| `09c` | [Measuring Spatial Inequality](notebooks/09c_spatial_inequality.ipynb) | Coefficient of variation vs standard deviation for comparing dispersion |
| | **Module 10 — Data Visualization and Communication** | |
| `10a` | [KDE and Density Estimation](notebooks/10a_kde.ipynb) | Kernel density estimation, bandwidth choice, and boundary artefacts |
| `10b` | [Ranked Bars, Annotation and Encoding](notebooks/10b_ranked_bars.ipynb) | Encoding choices as argument — what a chart claims before anyone reads it |
| `10c` | [Small Multiples](notebooks/10c_small_multiples.ipynb) | Repeated panels, the shared-axis rule, and reference lines |
| | **Module 11 — Policy and Domain Reasoning** | |
| `11a` | [The 'So What?' Test](notebooks/11a_evidence_classification.ipynb) | Classifying findings by what they license — action, monitoring, or context only |
| `11b` | [From Coefficient to Recommendation](notebooks/11b_coefficient_to_policy.ipynb) | Reading a confidence interval as a policy constraint |
| | **Module 12 — Advanced Synthesis** | |
| `12` | [Capstone — Choosing the Right Tool and Stating Honest Limits](notebooks/12_synthesis_capstone.ipynb) | Method selection and writing the scope of valid inference |

## Rebuilding

The notebooks are generated from `colab_pack/manifest.py` in the coursehub repo.
Edit the content modules there, not the `.ipynb` files:

```bash
python colab_pack/build_pack.py --check --zip
```

Every notebook is executed end to end as part of the build, so the worked
answers are known to reproduce the figures quoted in the course.

## African / Digital Humanities adaptation

If you want to repurpose this pack for African migration and Digital Humanities
research, the cleanest path is to keep the same method-first structure and swap
the substantive domain.

### Recommended data stack

| Layer | Suggested sources | Use |
|---|---|---|
| Migration microdata | IPUMS International, national census extracts | Internal migration, birthplace, residence, education, work |
| Cross-border migration | UN DESA migrant stock, OECD DIOC, Eurostat, US Census ACS / IPUMS USA, Statistics Canada | Africans in Europe and North America |
| African context | Afrobarometer, WorldPop, GHSL, UNHCR, ACLED | Attitudes, urbanisation, displacement, conflict context |
| DH text layer | African newspaper archives, oral histories, parliamentary debates, literary metadata | Discourse, identity, belonging, and public framing |

### Suggested project spine

Center the pack on migration and belonging in African cities. That keeps the data
African-based, supports spatial and statistical methods, and leaves room for a
genuine humanities layer through text and discourse analysis.

### Notebook translation

The current notebook arc can be adapted with only the subject matter changed:

| Current pattern | African / DH version |
|---|---|
| First look at the housing data | First look at migration in African cities |
| Absence audit | Reading data for what is missing |
| Group comparison | Migrants vs non-migrants, or cities and regions |
| Join keys and missingness | Integrating census, survey, spatial, and text sources |
| Regression and fixed effects | Explaining migration outcomes with place controls |
| Clustering and ML | Typologies of cities, corridors, or texts |
| Index construction | Belonging, mobility, or exclusion index |
| Spatial analysis | Urban growth, accessibility, and corridor geography |
| Policy reasoning | Evidence limits and interpretive scope |

### Practical implementation rule

Keep each notebook self-contained, use one main table per notebook, and end each
one with a short statement of what the method can and cannot support. That keeps
the adaptation aligned with the original pack instead of turning into a loose
collection of examples.
