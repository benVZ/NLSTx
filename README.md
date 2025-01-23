# NLSTx Dataset: A subset of difficult lung nodules from the NLST database

This repository hosts the NLSTx dataset, as introduced in:  
**B. Veasey et al., "Lung nodule malignancy classification based on NLSTx Data," in Proc. IEEE 17th Int. Symp. on Biomedical Imaging (ISBI), pp. 1870–1874, IEEE, 2020.** 

The dataset is officially released as part of the publication:  
**B. Veasey and A.A. Amini., "Low-Rank Adaptation of Pre-trained Large Vision Models for Improved Lung Nodule Malignancy Classification," IEEE Open J. Eng. Med. Biol., 2025.**

---

## NLSTx Dataset Description

The NLSTx dataset was derived from the National Lung Screening Trial (NLST), which contains CT scan data for over 15,000 participants. The majority of scans in the NLST are normal and do not contain nodules. The NLSTx subset specifically focuses on nodules critical for improving prognosis by including challenging early-stage malignancies and benign nodules with clear annotations. Key aspects of the dataset:

- **Malignant Nodules**: Nodules that appeared benign during initial screenings but were later confirmed as malignant through biopsy.
- **Benign Nodules**: Nodules associated with subjects who had only a single nodule reported in the NLST clinical notes, ensuring accurate matching of clinical and imaging data.

Radiologists annotated the dataset using anatomical locations provided in the NLST clinical notes to identify specific, pixel-level nodule locations. Each nodule is marked with a bounding box on the axial slice with the largest diameter. To use this dataset, you must first download the raw NLST CT images that are freely available by request at [https://www.cancerimagingarchive.net/collection/nlst/]. The NLSTx dataset can then be generated using the pixel-level nodule locations in this repo.

### Dataset Summary

The NLSTx dataset comprises **857 nodules from distinct subjects**, divided into:  
- **207 malignant nodules**: From subjects each with two or three annual scans.  
- **650 benign nodules**: From subjects with three annual scans.  

### Scan and Resolution Details
- **Slice Thickness**: ≤ 2.5 mm (mean: 2.32 mm).  
- **In-Plane Resolution**: 0.48–0.89 mm (mean: 0.66 mm).  

### Nodule Statistics Across Time Points
Below is a summary of nodule diameters across three annual time points (t0, t1, t2):

| **Scan Point** | **Diameter (mm)**  | **Mean (mm)** | **Median (mm)** |
|----------------|--------------------|---------------|-----------------|
| **t0**         | 4.98 – 76.4        | 11.67         | 9.96            |
| **t1**         | 4.31 – 97.9        | 12.4          | 10.3            |
| **t2**         | 4.52 – 91.6        | 12.3          | 10.1            |

This table highlights the nodule growth and variability over successive time points. The smaller minimum diameter at t1 reflects the possibility of new nodules appearing that were not present in t0.

---

## Citation

If you use this dataset in your work, please cite the following papers:

1. **NLSTx Introduction**:  
   ```bibtex
   @inproceedings{veasey2020nlstx,
      author    = {B. Veasey and M.M. Farhangi and H. Frigui and J. Broadhead and M. Dahle and A. Pezeshk and A. Seow and A. A. Amini},
      title     = {Lung nodule malignancy classification based on NLSTx Data},
      booktitle = {Proc. IEEE 17th Int. Symp. on Biomedical Imaging (ISBI)},
      pages     = {1870--1874},
      year      = {2020},
      publisher = {IEEE}
   }
2. **NLSTx Official Release**:  
   ```bibtex
   @article{veasey2025low,
      author    = {B. Veasey and A.A. Amini},
      title     = {Low-Rank Adaptation of Pre-trained Large Vision Models for Improved Lung Nodule Malignancy Classification},
      journal   = {IEEE Open Journal of Engineering in Medicine and Biology},
      year      = {2025},
      publisher = {IEEE}
   }
