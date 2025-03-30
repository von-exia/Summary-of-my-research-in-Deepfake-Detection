# Summary of my research in Deepfake Detection
## 🐋 Personal Introduction
```
Caibo Feng, Mar 2025
gn001_888@163.com; CaiBoFengEXIA@outlook.com
```
Maybe I won, maybe I failed. Whatever, I can only keep going.㊗️
I am currently a master student, whose research interest focuses on Deepfake Detection.
I am seeking opportunities of job. If you are interested in my work, please feel free to contact me.🤝

## Update table
v0.1 - 15 Mar 2025

## 👀 Overview of Content
- [Task brief](#intro)
- [Existing problems](#problem)
- [Future orientations](#future)
--[Major orientations](#major)
--[Minor orientations](#minor)
- [Value for society and business](#value)
---

<a id="intro"></a>
## 1. Task brief
Deepfake techniques bring a significant risk to face recognition system, but existing Deepfake Detection (DfD) methods are often overfitted to the specific forgery patterns from the training samples, and thus perform poorly on unseen samples. Concretely, DfD is a simple binary classification task, but it is not that simple as we think. Followings are a pair of real/fake images from popular FF++ training set. Usually, the existing works adopt the pre-trained face detection model to crop the face region for the deepfake detector. Since this preprocessing operation make the detector focus on learning the forgery clues around face region.

## Pair of real and fake images forged by Deepfake from FF++ dataset

| Real Face                    | Fake Face                    |
|-------------------------------|-------------------------------|
| ![Real](./img/r.png)  | ![Fake](./img/f.png)   |


<a id="problem"></a>
## 2. Existing problems
### (1) ⚠️ Outdated datasets
#### i. Low forgery quality
Almost all of the existing works training their detectors on the popular FF++ ddataset for fair comparison. However, it is a dataset that released in 2019! The fake images here (see above figure) is so easy to detect, even by human eyes.
#### ii. Few forgery patterns
On the other hand, the FF++ dataset provides the fake images forged by 4️⃣ fogery methods, which means it only contains four forgery patterns. It is insufficient to train a relatively useful detector for now.
#### iii. Stop the step to incoporate more training data
In order to publish papers, researchers still only conduct their experiments on FF++. Personally speaking, it is so boring. This practice is harmful to develop a practical deepfake detector, and stops our steps to go forward.
### (2) 🫥 Different bounding boxes to crop face
The authors of different papers crop the faces in the training and test datasets with different bounding boxes. Some authors crop the face regions with more background, but some authors may solely crop the face region with less background. This practice effects the final performance of detectors with different backbones (CNN or ViT). Additionally, it also makes the comparison unfair.
### (3) 😶‍🌫️ Impractical evaluation metrics
AUC, AP, EER are the most used metric in the papers of DfD. Since they demonstrate the comprehensive performance of detectors. Nevertheless, the accuracy (ACC) of almost every methods is low, which means these detectors still have no power to deal with the samples from different domains，and can not be put into the real-world scenario.
### (4) 🙄 More diverse forgery samples do not always bring better performance
When training the detectors with the latest DF40 dataset, you will find the detectors perform worse on the relatively old test sets (e.g. DFDCP, DFDC, DFD, WDF, etc.). This situation means that there is a large gap between the forgery patterns of old and new forgery methods. Then, here comes a question: is a single detector suficcent to solve all forgery samples? 
### (5) 🤥 Lack interpretebility
Currently, CLIP-ViT is discovered as the best backbone of the detectors. However, some work proves that ViT recognizes the real/fake images via high-level semantic information, instead of low-level forgery clues. The high-level semantic information is difficult to explain, and human eyes can not distinguish between real/fake images. Therefore, it is hard for us to annotate the text description for a fake face image, which means we can not re-train a backbone like CLIP or LLaVA with image-text pairs.

<a id="future"></a>
## 3. Future orientations
<a id="major"></a>
### (1) ⚠️ Major orientations (importance is down from top to bottom)
#### i. More effective learning methodd for DfD (or for other vision task)

#### ii. Data cleaning and annotation methods

#### iii. High quality image pairs of real and fake images

#### iv. Model updating methodd to handle constantly incremental forgery patterns (like a planning agent)

<a id="minor"></a>
### (2) ⚠️ Minor orientations
#### i. Specific and useful vision backbone for DfD

#### ii. Generally effective data augmentation methods


<a id="value"></a>
## 4. Value for society and business
TBD

