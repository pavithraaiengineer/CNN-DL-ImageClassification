# Image Classification with CNN

Build a Convolutional Neural Network (CNN) model to classify images from the CIFAR-10 dataset into 10 predefined categories through iterative architectural improvements and advanced training techniques.

[Repository link](https://github.com/pavithraaiengineer/CNN-DL-ImageClassification)

## Project Results
In this project, we processed the CIFAR-10 dataset and explored the results of 10 different classifier iterations:
* Models #1 - #4: Building sequential CNN models from scratch.
* Models #5 - #8: Deepening architecture and implementing Global Average Pooling.
* Model #9: Transfer learning and fine-tuning using EfficientNetB0.
* Model #10: Ensemble,
* Deployment for final prediction.

## Repository Folders and Files

### Documents
* **Presentation Slides**
* **Read me file**
* **10 notebooks with diferent models**

---

## Technical Evolution & Performance

```diff
# Training Progress Log
- Model #1: Baseline (2 Conv layers) -> Test Acc: 55.70%
- Model #2: Added BN and Dropout -> Test Acc: 62.63%
+ Model #3: Optimized 32x32 + BN -> Test Acc: 82.15%
+ Model #4: 6 Conv layers + L2 Reg -> Test Acc: 81.00%
+ Model #6: 13 Conv layers + GAP -> Test Acc: 93.03%
+ Model #7: Contrast Aug + AdamW -> Test Acc: 93.12%
+ Model #8: Brightnes augmentation. + AdamW -> Test Acc: 93.12%
+ Model #9: Transfer Learning (EfficientNetB0) -> Test Acc: 91.35%
+ Model #10: Final Ensemble for Maximum Stability 93.21%

---
## PROBLEMS & CHALLENGES

```diff
- Overfitting: High training accuracy but failed to generalize to the test set.
- Class Weakness: "Cat" and "Dog" categories had the lowest performance.
- Recall Drop: Cat/Dog recall declined continuously during training iterations.
- Feature Extraction: Baseline model was too shallow to capture complex image patterns.
- Data Quality: 32x32 resolution was too low and blurry for distinct classification.

---
## Recommended Notebooks
To see the best performing results and the final architecture, we recommend starting with these notebooks:

```diff
+ Recommended: model_7_training (Best Single Model)
+ Recommended: model_10_ensemble (Final Ensemble Strategy & Deployment)
! Note: Model 7 provides the highest individual accuracy, while Model 10 
! offers the most stable predictions on unseen data and highest accuracy.

## Installation & Setup

To replicate the environment and run the notebooks, follow these steps:

```bash
# 1. Create a virtual environment
python -m venv .venv

# 2. Activate the environment
# On Windows:
.venv\Scripts\activate
# On macOS/Linux:
source .venv/bin/activate
