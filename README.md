# DiCNet
This repository provides the PyTorch implementation of the paper: [Anomaly Discovery in Semantic Segmentation via Distillation Comparison Networks](https://arxiv.org/abs/2112.09908)

## Introduction
Our key observation is that semantic classification plays a critical role in existing approaches, while the incorrectly classified pixels are easily regarded as anomalies. Such a phenomenon frequently appears and is rarely discussed, which significantly reduces the performance of anomaly discovery. To this end, we propose a novel Distillation Comparison Network (DiCNet). It comprises of a teacher branch which is a semantic segmentation network that removed the semantic classification head, and a student branch that is distilled from the teacher branch through a distribution distillation. We show that the distillation guarantees the semantic features of the two branches hold consistency in the known classes, while reflect inconsistency in the unknown class. Therefore, we leverage the semantic feature discrepancy between the two branches to discover the anomalies. DiCNet abandons the semantic classification head in the inference process, and hence significantly alleviates the issue caused by incorrect semantic classification.

## How to use
### Environment
* Python 3.8
* Pytorch 1.10
### Install
#### Create a virtual environment and activate it
```
conda create -n dicnet python=3.8
conda activate dicnet
```
#### Dependencies
```
conda install pytorch torchvision torchaudio cudatoolkit=11.1 -c pytorch -c nvidia
pip install opencv-python
pip install numpy
pip install tqdm
pip install matplotlib
pip install easydict
pip install scipy
pip install scikit-learn
```

### Data Preparation
Download [StreetHazards train](https://people.eecs.berkeley.edu/~hendrycks/streethazards_train.tar), [StreetHazards test](https://people.eecs.berkeley.edu/~hendrycks/streethazards_test.tar)

### Train
Use [this repository](https://github.com/CSAILVision/semantic-segmentation-pytorch/tree/5c2e9f6f3a231ae9ea150a0019d161fe2896efcf)  to train a pspnet as the teacher network
























