# MScA_Machine_Learning_Project



## Data Description

Link: https://archive.ics.uci.edu/ml/datasets/Deepfakes%3A+Medical+Image+Tamper+Detection#

Attackers have the ability to intercept and add/remove medical evidence in medical imagery with high realism using deep learning. In this dataset we present medical deepfakes: 3D CT scans of human lungs, where some have been tampered with real cancer removed and with fake cancer injected. The objective of this dataset is to distinguish between real and fake cancers, and identify where medical scans have been tampered. Three expert radiologists have evaluated this dataset and could not reliably tell the difference between real and fake cancers, meaning that the fake cancers are realistic and this detection task is very challenging. For more information, please see our paper 'CT-GAN'.

The dataset consists of two sets (80 scans and 20 scans). The first 80 were used in a blind trial with the radiologists (they weren't told they were tampered), and the 20 scans were used in an open trial with the radiologists (they were told the truth and asked to identify them).

Provided with the scans is a table with the ground truth. For each scan, where a cancer is located (x, y, and z [slice#]) and its classification. A location can be classified as being:
True-Benign, (TB): A location that actually has no cancer
True-Malicious (TM): A location that has real cancer
False-Benign (FB): A location that has real cancer, but it was removed.
False-Malicious (FM): A location that does not have cancer, but fake cancer was injected there.

## Attribute Information

Each scan is in the medical dicom format, but it can be loaded as a 3D matrix with Python by using the tools provided in our code repository.

A scan is basically a series of 512x512 images. The series is usually about 100-300 slices long (the z axis). Cancers can occupy multiple slices along the z-axis.
The value at each pixel is the Hounsfield unit (radiodensity) at that location.
