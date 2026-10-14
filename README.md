# crime-rate-clustering-hierarchical-analysis
Spatial and demographic crime analysis using Hierarchical Clustering on state-level crime statistics (crime_data.csv) to support resource allocation and policymaking.

# Crime Rate Clustering using Hierarchical Clustering

## 1. Business Problem
### 1.1. Business Objective
To group states/regions (`crime_data.csv`) based on violent and property crime rates (Murder, Assault, Rape) along with urban population percentages. This helps law enforcement agencies, government bodies, and policymakers identify regional crime patterns and allocate security resources efficiently.
### 1.2. Constraints
* Discrepancies in state reporting standards and population scale require proper normalization.
* Subjectivity in defining high-risk zones requires clear, data-driven thresholds.

## 2. Data Dictionary
| Feature Name | Data Type | Description |
| --- | --- | --- |
| `State` | Categorical | Name of the US State |
| `Murder` | Numerical | Murder arrests per 100,000 residents |
| `Assault` | Numerical | Assault arrests per 100,000 residents |
| `UrbanPop` | Numerical | Percentage of the population living in urban areas |
| `Rape` | Numerical | Rape arrests per 100,000 residents |

## 3. Data Pre-processing
* **Data Cleaning:** Verified completeness of dataset and handled the `State` column by setting it as the DataFrame index for proper labeling.
* **Normalization:** Applied standard scaling to ensure features measured on different scales (e.g., `Assault` numbers vs. `UrbanPop` percentages) contribute equally to distance calculations.

## 4. Exploratory Data Analysis (EDA)
* **Summary:** Mean, median, and variance of crime rates across states.
* **Univariate Analysis:** Density plots and boxplots for murder, assault, and rape statistics.
* **Bivariate Analysis:** Pairplots and correlation matrices showing relationships between urbanization and violent crime rates.

## 5. Model Building
* **5.1 Scaled Data Models:** Implemented hierarchical agglomerative clustering utilizing Ward's method and Euclidean distance.
* **5.2 Dendrograms:** Generated dendrograms to visualize hierarchical merging and select the optimal cluster cutoff height.
* **5.3 Validation & Inferences:** Labeled clusters (e.g., High-Crime vs. Low-Crime regions) and evaluated cluster separations.

## 6. Business Benefits & Impact
* Optimized deployment of law enforcement personnel and emergency response units.
* Data-backed allocation of social welfare and crime-prevention grants to high-risk areas.
