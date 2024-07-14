# Machine Learning Methods in Radiomics for Cardiovascular Imaging Analysis

---

## Abstract
This article explores the application of machine learning techniques in nuclear medicine to analyze cardiovascular images. The work encompasses the segmentation of the affected heart area on polar maps, extraction of radiomic features from the ROI, and classification of patients into healthy individuals and those with abnormalities. Initial study results and the first stage of work are also presented.

---

## Introduction
Radiomics is a relatively new field in radiology aimed at extracting quantitative features from medical images. Machine learning and artificial intelligence techniques, when combined with radiomics, not only facilitate the extraction of numerical characteristics but also enable the processing of large data volumes, which is challenging with traditional methods.

This study examines the application of radiomics and machine learning methods for analyzing images obtained through myocardial perfusion scintigraphy. The objective is to develop a mathematical model for myocardial tissue analysis based on radiomic features.

---

## Experimental Part

The work involved segmenting the heart region on polar maps using various methods:

1. **U-Net for Segmentation**: A U-Net neural network was trained to improve the accuracy of myocardial polar map segmentation. This method provided additional flexibility and efficiency compared to traditional methods.
2. **K-means**: The K-means method was used for image clustering, allowing the image to be divided into clusters by minimizing within-cluster variance.
3. **Otsu Method**: The Otsu method was applied for automatic thresholding, optimally separating the image into background and object.
4. **Color Masking**: A color masking method was implemented to highlight the region of interest based on color characteristics, particularly useful for isolating specific areas in the image.

Comparing these methods provided data for selecting the optimal approach for polar map segmentation.

---

**Note**: Training U-Net and employing various segmentation methods offered additional tools for precise and efficient image processing within this project.

### Extraction of Radiomic Features from the Region of Interest (ROI)

The PyRadiomics library was used to extract radiomic features from the region of interest (ROI). This library offers tools for computing an extensive set of quantitative characteristics related to shape, texture, and pixel intensity in medical images.

#### About the PyRadiomics Library

PyRadiomics provides an implementation of the radiomic feature extraction standard proposed in [1]. This standard defines a large set of features, including:

- **First Order**: Statistics based on pixel intensity (mean, median, minimum, maximum, etc.).
- **Shape**: Features related to the geometric properties of the region of interest.
- **Texture Features**: Characteristics describing the texture diversity within the ROI.
- **Matrix Features**: Features based on gray level co-occurrence matrix and other matrices.

PyRadiomics also allows for customization of feature extraction parameters, enabling adaptation of the process to specific needs and characteristics of the images being processed.

Using PyRadiomics in this project allowed for the systematic extraction and analysis of radiomic features from myocardial polar maps.

---

**Note**: More detailed information about the PyRadiomics library can be found in the [official documentation](https://pyradiomics.readthedocs.io/).

---

Additionally, patient classification into healthy and abnormal categories was performed using machine learning methods.

The results of model testing are presented in Table 1:

| Model                     | Accuracy | Precision | Recall | F1-score |
|---------------------------|----------|-----------|--------|----------|
| Random Forest Classifier  | 0.74     | 0.81      | 0.81   | 0.81     |
| Decision Tree Classifier  | 0.71     | 0.80      | 0.69   | 0.74     |
| Blending Ensemble         | 0.68     | 0.74      | 0.81   | 0.77     |

---

## Conclusion
Various models were trained and analyzed, with the RandomForestClassifier model demonstrating the best results. The project aims to automate the processing of medical images using machine learning methods to extract quantitative information from diagnostic images.

---

## References
1. B. Kocak, E.S. Durmaz, E. Ates, O. Kilickesmez. Radiomics with artificial intelligence: a practical guide for beginners. Affiliation: Department of Radiology Istanbul Training and Research Hospital, İstanbul, Turkey. 2019 Nov;25(6): 485–495.
2. M. E. Mayerhoefer, A. Materka, G. Langs, I. Häggström, P. Szczypiński, P. Gibbs, G. Cook. Introduction to Radiomics. Citation: Journal of Nuclear Medicine April 2020, 61(4): 488-495.
3. B. A. Varghese, S. Y. Cen, D. H. Hwang, V. A. Duddalwar. Texture Analysis of Imaging: What Radiologists Need to Know. Citation: American Journal of Roentgenology. 2019;212: 520-528.
4. C. Hassani, F. Saremi, B. A. Varghese, V. Duddalwar. Myocardial Radiomics in Cardiac MRI. Citation: American Journal of Roentgenology. 2020;214: 536-545.
