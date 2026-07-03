# Flood Risk Exposure Mapping using Synthetic Data Generation

## Overview

This project develops a scalable synthetic data generator that simulates flood risk exposure and damage outcomes across locations in the Philippines. Rather than relying on existing datasets, the project constructs a statistically realistic multi-table dataset by modeling the relationships between geography, rainfall, infrastructure, socioeconomic conditions, and flood damage.

The project was developed during the **Eskwelabs Innovation Fellowship** as part of a data modeling and synthetic data generation initiative.

---

## Objectives

The project aims to:

* Generate realistic synthetic flood-risk datasets for the Philippines.
* Preserve meaningful statistical relationships between environmental and socioeconomic variables.
* Produce datasets suitable for exploratory data analysis (EDA), machine learning, and disaster-risk modeling.
* Create reproducible datasets for educational and research purposes without relying on sensitive real-world data.

---

## Dataset Structure

The generated dataset consists of five relational tables:

| Table                 | Description                                                                          |
| --------------------- | ------------------------------------------------------------------------------------ |
| **Locations**         | Geographic coordinates, population, urbanization, wealth, and vegetation information |
| **Elevation Proxies** | Elevation, slope, distance to water, and flood susceptibility                        |
| **Rainfall Events**   | Simulated rainfall events, seasons, duration, and rainfall intensity                 |
| **Assets**            | Simulated residential, commercial, infrastructure, and vehicle assets                |
| **Damage Reports**    | Flood damage occurrence, estimated losses, and damage severity                       |

The generator is capable of producing datasets containing millions of records while preserving realistic relationships across tables.

---

## Modeling Approach

The dataset is generated using a structural probabilistic model rather than random sampling.

The overall causal framework is

```
Location
    ↓
Socioeconomic Variables
    ↓
Environmental Variables
    ↓
Rainfall Events
    ↓
Flood Risk
    ↓
Assets
    ↓
Damage Reports
```

Key modeling techniques include:

* Log-normal distributions for population
* Poisson distributions for asset generation
* Gamma and Exponential distributions for environmental variables
* Logistic (sigmoid) models for flood susceptibility
* Gaussian noise for realistic variability
* Latent variables representing flood control and soil drainage

The resulting synthetic data exhibits realistic dependencies while remaining computationally efficient.

---

## Technologies Used

* Python
* NumPy
* Pandas
* SciPy
* Matplotlib
* Google Colab

---

## Features

* Synthetic dataset generation with millions of rows
* Probabilistic flood-risk simulation
* Multi-table relational database structure
* Environmental and socioeconomic dependency modeling
* Parameterized rainfall generation
* Flood damage estimation
* Dataset validation through exploratory data analysis

---

## Validation

The generated datasets were evaluated using exploratory data analysis and statistical validation.

The model demonstrates:

* Realistic rainfall distributions
* Spatial variability across Philippine regions
* Correlated environmental variables
* Heavy-tailed socioeconomic distributions
* Non-uniform flood risk patterns
* Plausible damage estimates

Overall, the generated data is suitable for educational, analytical, and predictive modeling applications.

---

## Applications

Potential use cases include:

* Flood risk assessment
* Machine learning
* Disaster response planning
* Geospatial analysis
* Predictive analytics
* Educational datasets for EDA and statistical modeling

---

## Repository Structure

```
├── Dataset_Generator.ipynb
├── Dataset_Validation.ipynb
├── README.md
├── sample_dataset.csv
```

---

## Future Improvements

Future work includes:

* Integration with GIS and Digital Elevation Model (DEM) data
* More realistic spatial distributions
* Additional measurement noise and missing-value mechanisms
* Stronger nonlinear relationships
* More extreme flood scenarios

---

## Author

**Jerick L. Garcia**

Bachelor of Science in Mathematics
University of the Philippines Diliman

Eskwelabs Innovation Fellow
