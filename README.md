# PCVC
#### **Persian Consonant Vowel Combination**  
If you want to use this dataset please reference to this paper:  
[Saber MalekzadeH, Mohammad Hossein Gholizadeh, Seyed Naser Razavi “Full Persian Vowel recognition with MFCC and ANN on PCVC speech dataset” 5th International conference of electrical engineering, computer science and information technology, Iran, Tehran, 2018.](https://scholar.google.com/citations?user=AVMa3t0AAAAJ&hl=en#d=gs_md_cita-d&p=&u=%2Fcitations%3Fview_op%3Dview_citation%26hl%3Den%26user%3DAVMa3t0AAAAJ%26citation_for_view%3DAVMa3t0AAAAJ%3AIjCSPb-OGe4C%26tzom%3D-270)

## About
This dataset is the first phoneme based speech dataset in the entire world and also the first free Persian speech dataset to help Persian speech researchers. It is not only this. It is growing...  
If you have any idea or time or file to help us grow this, Please Contact us at:  
URL: http://SMalek.blog.ir (Left part. "Contact" Side bar)

## What it is
This dataset contains of 23 Persian consonants and 6 vowels. The sound samples are all possible combinations of vowels and consonants (138 samples for each speaker). The sample rate of all 2 seconds speech samples is 48000 which means there are 48000 sound samples in every 1 second. Every sound sample is 2 seconds, which in average, 0.5 second of each sample is speech and the rest is silence. In every sound sample 0.25s of start and 0.25s of end of it is surely scilence.

Phoneme List in PCVC dataset:
[Here](https://github.com/S-Malek/PCVC/blob/master/PhonemeList.JPG)


## How to use
### Matlab
All files are ".mat" files. ".mat" is a fromat for data files in Matlab. Every file consists of a matrix with dimensions 1*23*6*30000 in which 23 is refer to number of consonant, 6 is refer to number of vowel and 30000 is the length of sound sample. order of phonemes are just like shown in [Here](https://github.com/S-Malek/PCVC/blob/master/PhonemeList.JPG). To use it, just open the file and tap on "finish" button to import the data in workspace of Matlab.

### Python
To use ".mat" data files in Python you can use the code below to copy the matrix in the file in "aud" variable (Put your current path instead of "MyPath"). Every file consists of a matrix with dimensions 1*23*6*30000 in which 23 is refer to number of consonant, 6 is refer to number of vowel and 30000 is the length of sound sample. order of phonemes are just like shown in [Here](https://github.com/S-Malek/PCVC/blob/master/PhonemeList.JPG).
```
import urllib.request as urllib2
matfile = urllib2.urlopen("https://raw.githubusercontent.com/S-Malek/PCVC/master/Samples/S1.mat")
with open('Speaker1.mat','wb') as output:
  output.write(matfile.read())
```
```
import scipy.io  
mat = scipy.io.loadmat('MyPath/S1.mat')  
aud=(mat['aud'])
```

## Acknowledgement
So many thanks to those helped us to develop PCVC dataset especially speakers: Farideh Jabraili, Hedayat Malekzadeh, Hamed
Afjuland, Mohammad Ataeizadeh, Tahereh Salari, Alireza Aghaei, Parisa Seyfpour, Sahel Soltani, Mina Bayarash, Milad Abdollahzadeh, Sadra Malekzadeh,...
