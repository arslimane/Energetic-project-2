# Abstract
This study addresses the crucial challenge of monitoring the State of Health (SOH) of Lithium- Ion Batteries (LIBs) in response to the escalating demand for renewable energy systems and the imperative to reduce CO2 emissions. The research introduces deep learning (DL) models, namely Encoder-Long Short-Term Memory (E-LSTM) and Convolutional Neural Network-LSTM (CNN-LSTM), each designed to forecast battery SOH. E-LSTM integrates an encoder for dimensionality reduction and a LSTM model to capture data dependencies. CNN-LSTM, on the other hand, employs CNN layers for encoding followed by LSTM layers for precise SOH estimation. Significantly, we prioritize model explanability by employing a game-theoretic approach known as SHapley Additive exPlanations (Shap) to elucidate the output of our models. Furthermore, a method based on pattern mining was developed, synergizing with the model, to identify patterns contributing to abnormal SOH decrease. These insights are presented through informative plots. The proposed approach relies on the battery dataset from the Massachusetts Institute of Technology (MIT) and showcases promising results in accurately predicting SOH values, in which the E-LSTM model outperformed the CNN-LSTM model with a Mean Absolute Error (MAE) of less than 1%.

## Introduction
This repo contains code for the paper: Data-Driven Strategy for State of Health Prediction and Anomaly Detection in Lithium-Ion
Batteries
```latex
@article{slimane2024,
  title={Data-Driven Strategy for State of Health Prediction and Anomaly Detection in Lithium-Ion
Batteries},
  author={Slimane Arbaoui, Ahmed Samet, Ali Ayadi, Tedjani Mesbahi, Romuald Boné},
  journal={Energy and AI},
  year={2024}
}
```
### Requirements

* python>=3.10.10
* tensorflow==2.11.1
* keras==2.11.0
* h5py==3.7.0


## How to Use
#### 1. Load the MIT Battery Dataset
- Download the following three files from the provided link [MIT](https://data.matr.io/1/projects/5c48dd2bc625d700019f3204):
     + '2017-05-12_batchdata_updated_struct_errorcorrect.mat'
     + '2017-06-30_batchdata_updated_struct_errorcorrect.mat'
     + '2018-04-12_batchdata_updated_struct_errorcorrect.mat'
     
     
- Execute the 'loading_data_MIT.ipynb' notebook, ensuring that the 'path_to_file' variable is set to the repository containing the downloaded files.
