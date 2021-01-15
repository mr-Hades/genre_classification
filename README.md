Task: Music Genre CLassification
Data description:
  Dataset : GTZAN (http://marsyas.info/downloads/datasets.html)
  Target: music genre (10 classes in this case like rock, metal classical, e.t.c)
  Data size: ex. 1.29 GB
  Data structure: wav files
  Experiments were run on a laptop having rtx 2060 (6gb) GPU
  Features used are extracted from a signal using mfcc for lstm,
                                                  aggregations of mfcc, spectral descriptors for SVM
  

Evaluation metrics: Accuracy.

# Signal classification

## Task</br>
Purpose of project is to classify differnet signal modulations. </br>

## Dataset</br>
I used public signal dataset 2016.10A, which is available in https://www.deepsig.ai/datasets.</br>
Targer classes are: 
'8PSK'
'AM-DSB'
'BPSK'
'CPFSK'
'GFSK'
'PAM4'
'QAM16'
'QAM64'
'QPSK'
'WBFM'
</br>
Data contains sequance of integers which desicribes our signal.</br>
Size is about 1.16G </br>
Input shape is (2, 128) </br>

Most of reaseach papers over this dataset are doing without any feature engineearing.
## Method </br>
CNN architecture is from  https://arxiv.org/pdf/1602.04105.pdf

## Feature engineearing </br>
In code there are two feature engineearing techniques,but best one performed raw data </br>
## Evaluation</br>
Architecture in paper was used without batch normalization trick. In my experiment I also added batch normalization before each activation function(right plot). See result in picture.</br>
NOTE: Images were ploted over test dataset.</br>
### SNR</br>
![Test Image 1](snr_formula.png) </br>
SNR is ratio between Power of signal and noise in decibels scale </br>
![Test Image 1](snr_db.png) </br></br></br>
![Test Image 1](snr.png)
![Test Image 2](batch_snr.png)</br></br>

## Run

For using ipython notebook you can download it and run through google colab, as computational resourseas are required.</br>
For each model (without and with batch norm) it require about 2 hours to train.
Ipython notebook contains script for downloading dataset.

www.deepsig.ai (https://www.deepsig.ai/datasets)
RF Datasets For Machine Learning | DeepSig
DeepSig has created RF datasets to aid in machine learning. These datasets can be used for original and reproducible research and experimentation.
