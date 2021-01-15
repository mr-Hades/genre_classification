# Music Genre CLassification

## Task</br>
Purpose of project is to classify genres of the given songs. </br>

## Dataset</br>
I used public signal dataset GTZAN, which is available in http://marsyas.info/downloads/datasets.html.</br>
Target classes are music genres (10 classes in this case like rock, metal classical, e.t.c) 
</br>
Data contains sequance of integers which desicribes our signal. Data contains wav files of about 30 sec long, 100 for each genre.</br>
Size is about 1.29G </br>

## Feature engineearing </br>
Mfcc and spectral descriptors are used in the models.
</br>
## Experiment</br>
2 differrent approaches were tried.
</br>
  SVM + PCA on mfcc and spectral descriptors aggregations (like mean std skewness e.t.c)
  </br>
  LSTM on mfcc </br>

## Test data
I used test data that was found from the dataset by random sampling with 0.25 coef.
</br>
## Results
F1 score was used as a metric.
</br>
LSTM - train - 99% test-57 %
</br>
PCA + SVM - train - 97% test-70 %
</br>

## Run
All steps to run are implemented in the given notbooks.
</br>
## Summary
The main reason for the overfitting and low scores on the test data is that dataset is pretty small for the given task.
</br>
## Future work.
Try same approaches on a bigger and cleaner dataset.
</br>
