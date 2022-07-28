http://www.kaggle.com/c/yoy-mimics-2022

# Yum or Yuck Butterfly Mimics 2022

## Evaluation

The Scoring Metric used for this competition is Mean F-Score with a beta of 1.0 (Mean-F1)

![Mean F1 Score](https://github.com/KeithPinson/butterfly_mimics_2022_dataset/raw/main/DocResources/meanF1-score.jpg "Averaged F1") 

False-positives (FP) are particularly problematic for the objective. The objective is to out perform a bird and a FP could represent a bird eating a toxic butterfly – not good. For the role of classifying 6 butterflies, we experimented with adjusting the *beta* to increase the sensitivity to FP in the *precision* metric. We found a beta of 1.0 performed well and have chosen to leave it at that often used value. Experimenting with other common metrics, F1 performed well with our small dataset.

The dataset is of cropped and photogenic images of butterflies, for example butterflies with a torn wing are rare. Artificial neural networks can be very good at classifying these types of images. So, we anticipate very high-scores and ties. First, second, and third place will be determined only by Mean-F1 score.

## Submission Format

The `submission.csv` file should resemble:

```
image,name
goabc6e644,spicebush
gpcb27504e,viceroy
gsc64524dc,viceroy
guf6eae7c8,monarch
gw3d42f465,monarch
hh5ed30daf,tiger
⋮
```

The file consists of 2 columns: the image id (first) and butterfly species name (second). There should be only one row per butterfly image. The [YOYMimics-2022-dataset.pdf](https://github.com/KeithPinson/butterfly_mimics_2022_dataset/blob/main/YOYMimics-2022-dataset.pdf) document explains the dataset directory structure and file formats. In short, the image id is the name of the JPG image less ".jpg" (it identifies *X*). The species name: black, monarch, pipevine, spicebush, tiger, and viceroy; is the class label (it is *ŷ*).

---

Copyright © 2022 Keith Pinson
