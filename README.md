# Abstract
Lithium-ion batteries play a crucial role in powering various applications, including Electric Vehicles (EVs), underscoring the importance of accurately estimating their State Of Health (SOH) throughout their operational lifespan. This paper introduces two novel models: a Transformer (TOPS-SoH ) and a Long Short-Term Memory based (LSTM-OSoH ) for One-shot Prediction of SOH. The LSTM- OSoH excels in accuracy, achieving a Masked Mean Absolute Error (MMAE) of less than 0.01 for precise SOH estimation, while the TOPS-SoH demonstrates simplicity and efficiency, with accuracy comparable to state-of-the-art models. The TOPS-SoH model also offers additional interpretability by providing insights into the attention scores between inputs and outputs, highlighting the cycles used for estimation. These models were trained using the MIT battery dataset, with auto-encoders employed to reduce the dimensionality of the input data. Additionally, the models’ effectiveness was validated against a Bidirectional LSTM BiLSTM baseline, demonstrating superior performance in terms of lower MMAE, MMSE, and MAPE values, making them highly suitable for integration into Battery Management Systems (BMS). These findings contribute to advancing SOH estimation up to the End Of Life (EOL), which is crucial for ensuring the reliability and longevity of lithium-ion batteries in diverse applications.

## Introduction
This repo contains code for the paper: Dual-Model Approach for One-Shot Lithium-ion Battery State of Health Sequence Prediction
Batteries
```latex
@article{ARRAY-D-24-00176,
  title={Dual-Model Approach for One-Shot Lithium-ion Battery State of Health Sequence Prediction},
  author={Slimane Arbaoui, Ahmed Samet, Ali Ayadi, Tedjani Mesbahi, Romuald Boné},
  journal={ARRAY},
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
     
     
- Execute the 'Generating pickle files.ipynb' notebook, ensuring that the 'path_to_file' variable is set to the repository containing the downloaded files.
#### 3. Generate Models
Execute the 'model_generating_MIT.ipynb' notebook to train the E-LSTM and CNN-LSTM models. After completing this step, run the 'combined_model_MIT.ipynb' notebook to integrate the LSTM model with the encoder.
