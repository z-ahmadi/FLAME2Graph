# FLAMES2Graph: An Interpretable Federated Multivariate Time Series Classification Framework

![Capture](https://github.com/anonymousger/FLAME2Graph/assets/85762194/5cdc8321-bf1a-49d1-976f-4b09ff777d05)
Increasing privacy concerns have led to decentralized and federated machine learning techniques that allow individual clients to consult and train models collaboratively without sharing private information. Some of these applications, such as medical and healthcare, require the final decisions to be interpretable. One common form of data in these applications is multivariate time series, where deep neural networks, especially convolutional neural networks based approaches, have established excellent performance in their classification tasks. However, promising results and performance of deep learning models are a black box, and their decisions cannot always be guaranteed and trusted. While several approaches address the interpretability of deep learning models for multivariate time series data in a centralized environment, less effort has been made in a federated setting. In this work, we introduce FLAMES2Graph, a new horizontal federated learning framework designed to interpret the deep learning decisions of each client. FLAMES2Graph extracts and visualizes those input subsequences that are highly activated by a convolutional neural network. Besides, an evolution graph is created to capture the temporal dependencies between the extracted distinct subsequences. 
The federated learning clients only share this temporal evolution graph with the centralized server instead of trained model weights to create a global evolution graph. 
Our extensive experiments on various datasets from well-known multivariate benchmarks indicate that the FLAMES2Graph framework significantly outperforms other state-of-the-art federated methods while keeping privacy and augmenting network decision interpretation. 

## The data used in this project:
 * The Baydogan’s archive, contains 13 multivariate time series classification datasets. In this work, we choose five datasets from this archive (UWave, ECG, AUSLAN, NetFlow, and Wafer).
 * Human Activity Recognition (HAR) dataset recorded daily activities from 30 volunteers and produced six different labels of these activities (walking, walking upstairs, walking downstairs, standing, sitting, and lying).
 * PAMAP2 Physical Activity Monitoring (PAM) dataset recorded 18 different daily activities using 17 sensors. 
## Code
The code is divided as follows:

* The main.py python file contains the necessary code to run an experiement.
* The FlySmote.py contains the necessary functions to apply fly-smote re-balancing method.
* the NNModel.py contains the neural network model.
* The ReadData.py file contains the necessary functions to read the datasets.

To run a model on one dataset you should issue the following command:

```bash
python main.py -f <dataname> -d <data file name> -k <samples from miniority> -r <ratio of new samples>
```

## Prerequisites
The python packages needed are:
* numpy
* pandas
* sklearn
* scipy
* matplotlib
* tensorflow
* keras

## Reference
If you re-use this work, please cite:
```

```
