# CTS-LSTM

CTS-LSTM: LSTM-based neural networks for Correlated Time Series prediction

![The framework of CTS-LSTM](https://github.com/bettermia/CTSLSTM/blob/master/images/The%20framework%20of%20CTS-LSTM.png?raw=true)

<p align="center">Fig.1 The framework of CTS-LSTM</p>

![The structure of ST-cell](https://github.com/bettermia/CTSLSTM/blob/master/images/The%20structure%20of%20ST-cell.png?raw=true)
<p align="center">Fig.2 The structure of ST-cell</p>

# Dataset

The air quality dataset is scratched from a public [website](http://zx.bjmemc.com.cn/).

Statistics of the air quality dataset:

![Statistics of the air quality dataset](https://github.com/bettermia/CTSLSTM/blob/master/images/Statistics%20of%20the%20air%20quality%20dataset.png?raw=true)


We select 1st Jan. 2017 to 19th Nov. 2017 as the training set, and the remainders as the test set. 

The values of the sensors in a city are correlated in the spatial dimension since pollutants diffuse and aggregate gradually in the space. For each pollutant, we predict the values of all the sensors in the following day, thus the prediction time interval <a href="https://www.codecogs.com/eqnedit.php?latex=k&space;\in&space;\{1,\cdots,24\}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?k&space;\in&space;\{1,\cdots,24\}" title="k \in \{1,\cdots,24\}" /></a>.

The spatial relationship matrix <a href="https://www.codecogs.com/eqnedit.php?latex=S" target="_blank"><img src="https://latex.codecogs.com/gif.latex?S" title="S" /></a> is initialized by the reciprocal of distance between sensors.

Finally, we provide three air quality dataset:

- BeijingNO2

- BeijingO3

- LondonNO2

and two spatial relationship of sensors in Beijing and London:

  - beijingPriorMatirx
  - londonPriorMatirx



# Requirements

- python == 3.6
- Keras == 2.1.2
- TensorFlow == 1.7.0



# Usage

The model implement mainly lies in "CTSLSTM.py" which is well commented. 

Before running the code, you can modify the "HyperParameters.json" to  try other parameters or use other dataset to train or test the model.

To train and test our model on BeijingNO2 dataset, simply run the following command:

    python train.py



# Citing

If you find our work is helpful for your research, please kindly consider citing our paper as well:

    @article{wan2019cts,
    title={CTS-LSTM: LSTM-based neural networks for correlatedtime series prediction},
    author={Wan, Huaiyu and Guo, Shengnan and Yin, Kang and Liang, Xiaohui and Lin, Youfang},
    journal={Knowledge-Based Systems},
    year={2019},
    publisher={Elsevier}
    }