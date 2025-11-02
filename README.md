Neuroimaging_ScalingPipeline
This repository contains a collection of Jupyter notebooks for MRI image preprocessing, visualization, and analysis including intensity normalization, skull stripping, tumor segmentation, and contrast-based subtraction map generation.
The goal of this repository is to provide a reproducible pipeline for neuroimaging data exploration and quantitative analysis using open-access MRI datasets.
Dataset Used:
1.	BraTS-Africa
Dataset Descriptor: Adewole, M., Rudie, J.D., Gbadamosi, A., Zhang, D., Raymond, C., Ajigbotoshso, J., Toyobo, O., Aguh, K.,Omidiji, O., Akinola R., Suwaid, M.A., Emegoakor, A., Ojo, N., Kalaiwo, C., Babatunde, G., Ogunleye, A., Gbadamosi, Y.,Iorpagher, K., Onuwaje M., Betiku B., Saluja, R., Menze, B., Baid, U., Bakas, S., Dako, F., Fatade A., Anazodo, U.C. (2024) Expanding the Brain Tumor Segmentation (BraTS) data to include African Populations (BraTS-Africa) (version 1) [Dataset].The Cancer Imaging Archive. https://doi.org/10.7937/v8h6-8×67
Link: https://www.cancerimagingarchive.net/collection/brats-africa/
2.	UNC Paired 3T-7T MRI Dataset

Data Descriptor: Chen, X., Qu, L., Xie, Y. et al. A paired dataset of T1- and T2-weighted MRI at 3 Tesla and 7 Tesla. Sci Data 10, 489 (2023). https://doi.org/10.1038/s41597-023-02400-y
Link:https://springernature.figshare.com/articles/dataset/UNC_Paired_3T7T_Dataset/23706033?backTo=%2Fcollections%2FA_paired_dataset_of_T1_and_T2weighted_MRI_at_3_Tesla_and_7_Tesla%2F6485272&file=41605158

Notebooks
1.	Mri_Brain_Preprocessing_and_Contrast_EvaluationPurpose:
•	Load and visualize T1- and T2-weighted MRI images
•	Inspect image orientation, voxel shape, and intensity distribution
•	Perform skull stripping and intensity normalization
•	Generate addition and subtraction maps between T1 and T2 sequences to explore contrast differences.


2.	Glioma_Brain_Mri_Tumor_Localization_and_Area_MappingPurpose:
•	Load multimodal MRI data for Glioma subjects (T1, T2, T2-FLAIR, T1GD)
•	Isolate and visualize the tumor mask from segmentation maps
•	Compute tumor area per slice and identify:
o	The slice with the largest tumor area
o	The coordinates of the tumor region

3.	MR_Subtraction_Maps.ipynb
Purpose:
•	Generate subtraction maps between multiple MRI sequences to highlight intensity and contrast variations across modalities:
o	T1 − T2
o	T1 − T2FLAIR
o	T2 − T2FLAIR
o	T1GD − T1
o	T1GD − T2
o	T1GD − T2FLAIR
These maps help visualize tissue characteristics and can assist in detecting subtle differences in image contrast across modalities.

Key Features
•	Loading and orientation validation of MRI volumes (.nii/.nii.gz)
•	Skull stripping and intensity normalization
•	Tumor mask extraction and area quantification
•	Generation of inter-modality subtraction maps
•	Visual comparison of intensity and contrast patterns across MRI sequences



Dependencies
•	Python 3.8+
•	nibabel
•	numpy
•	matplotlib
•	scikit-image
•	nilearn (optional for visualization)
•	scipy
•	pandas
•	open-cv

Author
Barsa Rani Dey
📧 barsadey123@gmail.com
🔗 GitHub: barsa98


