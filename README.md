
# Cloud Coverage Detection

This project focuses on predicting the cloud coverage percentage for the next 15, 25, 30 minutes using deep learning models. We are given a complete training data file with extensive features and target variable values over a span of 11 months.


## Table of Contents

* [Models Implemented](#models-implemented)
* [Modifications and Enhancements](#modifications-and-enhancements)
* [Installation](#installations)

  
## Models Implemented

* **LSTM:** LSTM networks are particularly well-suited for sequential data as they can learn long-term dependencies and patterns over time.

* **GRU:** GRU is a simpler and more efficient alternative to LSTMs. It uses a gating mechanism to control the flow of information within the network.
  
* **TDNN:** Time delay neural networks (TDNNs) are a specific type of recurrent neural network architecture designed to handle sequential data, particularly time series data

* **Transformer:** The Transformer model leverages self-attention mechanisms to effectively capture relationships in sequential data.

## Modifications and Enhancements

To improve the `r2_score`, we created a custom architecture merging LSTM and GRU layers along with creating a meta learner for the trained models to give a final output. These modifications leveraged the strengths of each model to enhance performance

* **GRU-LSTM Model:** Integrated both GRU and LSTM for capturing short term and long term patterns separately. Outputs of both layers were passed to a dense layer to encode them for next layers.

* **Weighted Ensemble:** Created a voting based ensemble by specifying model's individual weights for the predictions.

* **Meta Learner:** Created a meta learner based on the individual predictions of the models to give a final prediction.


## Installation

To set up this project, clone the repository:

```bash
git clone https://github.com/vansh2101/cloud-coverage-detection.git
cd semantic-segmentation
```
    
