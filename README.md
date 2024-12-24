# MTGNN
This repository contains the implementation of the Multi-Track Graph Neural Network (MTGNN) as detailed in the paper titled **"Multi-Track Message Passing: Tackling Oversmoothing and Oversquashing in Graph Learning via Preventing Heterophily Mixing."** This work was presented at the forty-first International Conference on Machine Learning (ICML) in 2024, where it received a spotlight representation. 

## Brief Description of Code Structure
The code structure is organized as follows:

1. **pretrain**: This directory contains the auxiliary model, which helps in initializing the parameters effectively before the main training phase.

2. **src**: This directory includes the multi-track model implementation, encapsulating the core functionalities and algorithms of the MTGNN, designed to handle the challenges of oversmoothing and oversquashing in graph learning.

## Environmental Configuration

To set up the environment and install the necessary dependencies for running the code, execute the following command:

```bash
pip install -r requirements.txt
```

This will ensure that all required packages are installed and that your environment is correctly configured for the experiments.

## Instruction for Node Classification Experiment

To run the node classification experiment using the MTGNN implementation, you can use the following command:

```python
python mutil_stage_train.py --dataset='dataname' --a=0.9 --dr=0.5 --lr=0.01 --layer_num=64
```

### Parameters:

- **--dataset='dataname'**: Specify the dataset you want to use for the experiment. Make sure the dataset is properly formatted and available in the appropriate directory.

- **--a=0.9**: This parameter can be adjusted to control the influence of the message passing mechanism. A value of 0.9 indicates a strong reliance on message passing, which can be fine-tuned based on the specific characteristics of your dataset.

- **--dr=0.5**: This is the dropout rate applied during training. It helps prevent overfitting by randomly dropping a fraction of the nodes in the graph.

- **--lr=0.01**: The learning rate for the optimization algorithm. This rate can be tuned for better convergence during the training process.

- **--layer_num=64**: This parameter defines the number of layers in the model. Increasing the number of layers can capture more complex relationships in the graph but may also lead to issues like oversmoothing.

### Additional Information

For more details on the implementation and theoretical background, please refer to the original paper. If you encounter any issues or have questions regarding the code, feel free to open an issue in this repository. Contributions and feedback are welcome as we aim to improve the usability and performance of the MTGNN framework.