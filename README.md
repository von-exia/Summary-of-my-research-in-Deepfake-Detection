# Summary-of-my-research-in-Deepfake-Detection
## 🐋 Personal Introduction
```
Caibo Feng, Mar 2025
gn001_888@163.com; CaiBoFengEXIA@outlook.com
```
Maybe I won, maybe I failed. Whatever, I can only keep going.㊗️
I am currently a master student, whose research interest focuses on Deepfake Detection.
I am seeking opportunities of work. If you are interested in my work, please feel free to contact me.🤝

## 👀 Overview of Content
- [Task brief](#intro)
- [Existing problem](#problem)
- [Future work](#future)
- [Value for society and buisness](#value)

---

<a id="intro"></a>
## 1. Task brief
Deepfake techniques bring a significant risk to face recognition system, but existing Deepfake Detection (DfD) methods are often overfitted to the specific forgery patterns from the training samples, and thus perform poorly on unseen samples. Concretely, DfD is a simple binary classification task, but it is not that simple as we think. Followings are a pair of real/fake images from popular FF++ training set. Usually, the existing works adopt the pre-trained face detection model to crop the face region for the deepfake detector. Since this preprocessing operation make the detector focus on learning the forgery clues around face region.

## Pair of real and fake images forged by Deepfake from FF++ dataset

| Real Face                    | Fake Face                    |
|-------------------------------|-------------------------------|
| ![Real](./img/r.png)  | ![Fake](./img/f.png)   |


<a id="problem"></a>
## 2. Existing problem
### (1) ⚠️ Outdated datasets
#### i. Low forgery quality
Almost all of the existing works training their detectors on the popular FF++ ddataset for fair comparison. However, it is a dataset that released in 2019! The fake images here (see above figure) is so easy to detect, even by human eyes.
#### ii. Few forgery patterns
On the other hand, the FF++ dataset provides the fake images forged by 4️⃣ fogery methods, which means it only contains four forgery patterns. It is insufficient to train a relatively useful detector for now.
#### iii. Stop the step
In order to publish papers, researchers still only conduct their experiments on FF++. Personally speaking, it is so boring. This practice is harmful to develop a practical deepfake detector, and stops our steps to go forward.
### (2) 🫥 Different bounding box to crop face
### (3) 😶‍🌫️ Impractical evaluation metrics
AUC, AP, EER are the most used metric in the papers of DfD. Since it demonstrates the comprehensive performance of detectors. Nevertheless, the accuracy (ACC) of almost every methods is low, which means these detectors still have no power to deal with the samples from different domains.
### (4) 🙄 More diverse forgery samples do not bring better performance
### (5) 🤥 Lack interpretebility

<a id="future"></a>
## 3. Future work
这里是简介内容。

<a id="value"></a>
## 4. Value for society and buisness
这里是简介内容。

