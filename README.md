# TMN: An Efficient Robust Aggregator for Federated Learning
This repository contains the source code for MICAD2023 Publication "TMN: An Efficient Robust Aggregator for Federated Learning"

The Base code was cloned from [here](https://github.com/Naiftt/SPAFD)

# Abstract 
The collaboration of multiple organizations, such as hospitals, with access to data, can expedite the training process, resulting in superior machine learning models with increased data availability. However, the sensitivity of medical data poses challenges to information sharing without compromising privacy and confidentiality. Federated Learning (FL) offers a promising solution by enabling collaborative training through a data-sharing-free approach. Nevertheless, a large number of FL aggregation algorithms assume clients are honest, leaving the global model vulnerable to poisoning attacks. Approaches to safeguard against such attacks often add high computational costs, making them unsuitable for practical applications. In this work, we propose a robust aggregation rule, named Trimmed-Median Neighbourhood, for Byzantine-tolerant machine learning, offering computational efficiency and resilience to various attacks. Our method achieves up to a 2\% improvement over the baseline and modified approaches in an adversarial attack setting on a non-IID data split from the HAM10000 dataset while maintaining low computational requirements.

# Experimental Settings
## No Attack: 0 Byzantine Clients
## Attack 1: 3 Byzantine Clients
- Clinet 1: Random Noise
- Clinet 2: Random Noise
- Clinet 3: Random Noise
## Attack 2: 4 Byzantine Clients
- Clinet 1: Random Noise
- Clinet 2: Random Noise
- Clinet 3: 100 X Scaling
- Clinet 4: -1 X Scaling


# Install dependencies
```
pip install -r requirements.txt
```


# Download Dataset
The HAM10000 dataset can be used from [here](https://www.kaggle.com/kmader/skin-cancer-mnist-ham10000)

## Adding Dataset Path
Update the base_dir path in  **skinCancer_drich** function in the **dataset.py** <br /> 


# Running Experiments

## Run All Experimenets in No Attack Setting 
```
bash run_no_attack.sh
```

## Run All Experimenets in Attack-1 Setting 
```
bash run_attack_1.sh
```

## Run All Experimenets in Attack-2 Setting 
```
bash run_attack_2.sh
```
## Run Scaling Client Experimetns 
```
bash run_client_scaling.sh
```


# Results
Please run the **results.ipynb** to view plots and tables for all the experiments
