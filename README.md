# Deep Inversion Neural Network 

## Introduction
> A DNN method used for 1D seismic waveform inversion. 

The code is used for **waveform inversion**, which is built on **DNN method**. The DNN method is not iterative algorithm, so there is not no local minimum problem and it can present weight information through attention mechanism. 

This repository contains:

1. [Training code](train.py) used for training DNN.
2. [Testing code](test.py) used for test the trained model.
3. [Wave number code](None) to generate training data.
4. [Plots](plot.py) used for plot.


## Table of Contents

- [Deep Inversion Neural Network](#deep-inversion-neural-network)
  - [Introduction](#introduction)
  - [Table of Contents](#table-of-contents)
  - [Quick Start](#quick-start)
    - [Usage](#usage)
  - [Traning](#traning)
    - [Usage](#usage-1)
  - [Environment](#environment)
  - [Maintainers](#maintainers)
  - [Credit](#credit)

## Quick Start 
1. Download the DNN weights from [LOGS](None) 
2. Prepare the waveform as .npz file. 
3. Run valid. 

```
valid.py --model MODLE --input DATA_FILE
```

### Usage
```
valid.py [-h] [--model MODLE]
         [--input DATA_FILE] 
         [--output OUT_FILE]
positional arguments:
  --input        Waveform data file
  --output       Output path 
optional arguments:
  -h, --help         show this help message and exit
  --model MODEL      path to model weight file, default model/invnet
``` 

## Traning 
1. Make sure FK is installed. 
2. Or you can use the raw data. 

### Usage 
```
train.py [-h] [--fk PATH_TO_FK] 
         [--data PATH_TO_DATA] 
         [--model MODEL]
positional arguments:
  --fk        path to fk 
optional arguments:
  -h, --help         show this help message and exit
  --model MODEL      path to model weight file, default model
  --data PATH        path to data files. fk is not need if data is defined.
``` 

## Environment

This project uses [Tensorflow](http://tensorflow.com).

```sh
$ pip install tensorflow==1.13.1
```

## Maintainers

[@Cangye](https://github.com/cangyeone).


## Credit 
Crustal structures obtained from wavefrom modeling using deep neural network. 

**Abstract**
We present....