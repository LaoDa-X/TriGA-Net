# TriGA-Net
Pytorch implementation on: TriGA-Net: A Graph Attention Network for Brain-Controlled Speaker Extraction


## Introduction
The rapid development of auditory attention decoding (AAD) based on electroencephalography (EEG) signals offers the possibility of EEG-driven target speaker extraction. However, how to effectively utilize the target-speaker common information between EEG and speech remains an unresolved problem. To address this limitation, we propose A Graph Attention Network for Brain-Controlled Speaker Extraction (TriGA-Net), which utilizes the EEG recorded from the listener to extract the target speech. In order to effectively extract information from EEG signals, we derive multi-scale temporal–frequency features and further employ graph convolutional networks and a self-attention mechanism to effectively exploit the inherent graph-structured nature of EEG. In addition, to make full use of the fused EEG and speech features and preserve global context and capture speech rhythm and prosody, we introduce MossFormer2 which combines MossFormer and RNN-Free Recurrent as the separator. Experimental results on both the public Cocktail Party Dataset and KUL Dataset in this paper show that our TriGA-Net model significantly outper-forms the state-of-the-art method in certain objective evaluation metrics.
<p align="center">
<img width="1872" height="498" alt="image" src="https://github.com/user-attachments/assets/6b7e2040-f0b1-413a-af54-a69caa04e8bb" />
Figure 1. Overall Architecture
<p align="center">
<img width="1664" height="746" alt="image" src="https://github.com/user-attachments/assets/885e4e77-c2a6-4579-a2d7-a38058734d26" />
Figure 2. The EEG Encoder
<p align="center">
<img width="1480" height="932" alt="image" src="https://github.com/user-attachments/assets/a09ed193-28ea-44e9-a230-0e73ea62957a" />
Figure 3. The separator consists of two complementary submodules as illustrated in the figure. 


## Requiements
Python : 3.9.23

torch 2.5.1+cu118

## Datasets
The source and processing of the Cocktail Party dataset can be obtained [here](https://github.com/jzhangU/Basen)

KUL dataset can be obtained [here](https://zenodo.org/records/4004271)

## Code Availability
The training logs in this paper are available in the train_logs.txt.

The core source code for reproducing our results are available in the TriGA-Net.ipynb
