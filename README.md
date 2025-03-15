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
### (2) 🫥 Different bounding box to crop face
### (3) 😶‍🌫️ Impractical evaluation metrics
### (4) 🙄 More diverse forgery samples do not bring better performance
### (5) 🤥 Lack interpretebility

<a id="future"></a>
## 3. Future work
这里是简介内容。

<a id="value"></a>
## 4. Value for society and buisness
这里是简介内容。

