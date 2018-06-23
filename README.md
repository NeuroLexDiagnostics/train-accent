# train-accent

Github repo for training accents using common voice dataset. 

## how to download data

First, make sure ou have roughy 40-50 GB of hard disk space on your computer. 

Go to [this link]() and download the data with the arrow on the top right corner of the page. 

Feel free to explore and use different datasets as well. If you find any other datasets that are released under an open-source license, let us know and we'll post them here. 

## how the data is arranged

The data is arranged into many different accent types:

* african | african controls 
* australian | australian controls 
* bermuda | bermuda controls
* canada | canada controls 
* england | england controls
* hongkong | hongkong controls
* indian | indian controls
* ireland | ireland controls
* malaysia | malaysia controls
* new zealand | new zealand controls
* phillipines | phillipines controls
* scotland | scotland controls
* signapore | singapore controls
* southatlandtic | southatlandtic controls
* us | us controls
* wales | wales controls

Control groups are provided for each variable groups which is roughly an equal number of samples randomized from all the other groups. Both .wav files and .json feature arrays are provided to help you model the data. The .json feature arrays is composed of audio features (mfcc coefficients 1-13 and mfcc delta coefficients) extracted using the librosa library. Note these features can be used as a guide and you can come up with new feature embeddings to get better accuracy with your models (e.g. language models may be important here to reflect regional differences in speakers). 

## goals / what to beat 

Here are some goals (in terms of accuracy) to beat with the project. 

| Age model name | Accuracy | Standard Deviation | Modeltype | 
| ------------- | ------------- | ------------- | ------------- |
| us.pickle | 71.1% | +/- 1.0% | knn |
| indian.pickle | 79.9% | +/- 3.0% | knn | 
| england.pickle | 72.9% | +/- 0.8% | knn | 
| australia.pickle | 78.9% | +/- 1.3% | knn |
| canada.pickle | 77.9% | +/- 3.0% | knn| 

## references 
* [Common Voice Dataset](https://www.kaggle.com/mozillaorg/common-voice)
* [librosa](https://librosa.github.io/librosa/core.html#core)
* [spacy](https://spacy.io/)
