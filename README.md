# Targeting succinate metabolism to lower brain injury during mechanical thrombectomy in ischemic stroke

The notebook contains:
Metabolomics data of patients/mice from the brain tissue at different timepoints after ischemia (0min, 5min, 15min, 30min, 60min, 120min) that were analysed by liquid chromatography-mass spectrometry (LC-MS).

## Reproducibility
Code for the R analysis can be reproduced by following the script in `MetabolomicsAnalysis.Rmd`. This includes the data normalisation, differential metabolite analysis and all subsequent plots.

Metabolic signatures used for pathway analysis where manually assigned based on our a priori knowledge.

## Data
The Metabolomics data of will be deposited with the manuscript. LC-MS data aquistion has been performed by the Frezza Laboratory, CECAD Research Center, Faculty of Medicine, University Hospital Cologne, Germany. Input data will be available upon publication in the folder `"Input"`:

- `20211210_Amin_mousebrain_HAP02.csv` (Metabolomics results mouse)
- `20211212_Amin_humanbrain_HAP01.csv` (Metabolomics results patients)
- `MetabolicPathways.csv` (Metabolite names and associated pathways)

First we performed data filtering and normalisation (80%-filtering rule, missing value imputation, total/ion count normalisation) and outlier detection based on quality control (muma analysis, for details see html and folder `"Muma"`). The results will be saved in the folder `"Output/DataTables"`upon publication:

- `Human_TIC-normalised.csv`
- `Mouse_TIC-normalised.csv`

Using the normalised data, we removed the outliers and 
1. calculated the mean of the analytical replicates. The results will be saved in the folder `"Output/DataTables"`upon publication:

- `Human_TIC-normalised_Means.csv`
- `Mouse_TIC-normalised_Means.csv`

2. Performed differential metabolite analysis comparing `0min versus Xmin` using the mean data. Here we performed the t-Test and p-value adjustment using Benjamini Hochberg. The results will be saved in the folder `"Output/DataTables"`upon publication:

- `Human_TotalPools_DMA_5minv0min.csv`
- `Human_TotalPools_DMA_15minv0min.csv`
- `Human_TotalPools_DMA_60minv0min.csv`
- `Human_TotalPools_DMA_120minv0min.csv`

- `Mouse_TotalPools_DMA_5minv0min.csv`
- `Mouse_TotalPools_DMA_15minv0min.csv`
- `Mouse_TotalPools_DMA_60minv0min.csv`
- `Mouse_TotalPools_DMA_120minv0min.csv`

## Figures
Generated figures can be found in the html files or in the folder `"Output/Figures"`.
