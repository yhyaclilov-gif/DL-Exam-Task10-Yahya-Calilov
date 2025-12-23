# Task 10: Traffic Sign Recognition (GTSRB)

**Student:** Yahya Calilov 
**ID:** S210
**Task:** 10 – SignLang (Traffic Signs)

## Presentation
[View Presentation Slides](https://docs.google.com/presentation/d/1r4bDzN8_BVKITnh3K7Czfno3MdVGJWXk/edit?usp=sharing&ouid=114038006045355748570&rtpof=true&sd=true)

## Dataset
- **Name:** GTSRB (German Traffic Sign Recognition Benchmark)
- **Classes:** 10 selected traffic signs
- **Train samples:** ~7860
- **Test samples:** ~3750

## Selected Classes
0, 1, 2, 14, 17, 18, 25, 33, 34, 35

## Model Architecture
- **Base model:** MobileNetV2 (pretrained on ImageNet)
- **Frozen layers:** All backbone layers
- **Trainable layers:** Classifier only
- **Classifier:** Linear(1280 → 10)

## Training Comparison

### Version 1
- **Optimizer:** Adam
- **Learning rate:** 0.0001
- **Epochs:** 30
- **Test accuracy:** ~81%

### Version 2
- **Optimizer:** Adam
- **Learning rate:** 0.00001
- **Epochs:** 15
- **Test accuracy:** ~64%

### Best Result
- **Best version:** Version 1
- **Final test accuracy:** ~81%
- **Target accuracy:** 88%
- **Status:** Below target

## Analysis
Version 1 achieved better performance due to a higher learning rate, 
which allowed faster convergence of the classifier layer. 
Version 2 used a much smaller learning rate, resulting in slower learning 
and lower final accuracy.

## Results
- Training comparison plot
- Confusion matrix
- 10 sample predictions

