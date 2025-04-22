# PCVC
#### **Persian Consonant Vowel Combination**  
If you want to use this dataset please reference to this paper:  
[Saber MalekzadeH, Mohammad Hossein Gholizadeh, Seyed Naser Razavi “Full Persian Vowel recognition with MFCC and ANN on PCVC speech dataset” 5th International conference of electrical engineering, computer science and information technology, Iran, Tehran, 2018.](https://scholar.google.com/citations?user=AVMa3t0AAAAJ&hl=en#d=gs_md_cita-d&p=&u=%2Fcitations%3Fview_op%3Dview_citation%26hl%3Den%26user%3DAVMa3t0AAAAJ%26citation_for_view%3DAVMa3t0AAAAJ%3AIjCSPb-OGe4C%26tzom%3D-270) ([PDF](http://bayanbox.ir/download/2723849504007807268/Full-Persian-Vowel-recognition-with-MFCC-and-ANN-on-PCVC-speech-dataset.pdf))

If you have any idea or time or file to help us grow this, Please Contact us at:  
URL: https://smalekz.github.io


## About
This dataset is the first phoneme based speech dataset in the entire world and also the first free Persian speech dataset to help Persian speech researchers. It is not only what you see. It is growing. To be continued...  
## What it is
This dataset contains of 23 Persian consonants and 6 vowels. The sound samples are all possible combinations of vowels and consonants (138 samples for each speaker) with a length of 30000 data samples. The sample rate of all speech samples is 48000 which means there are 48000 sound samples in every 1 second. In each sample, sound starts with consonant and then there is a vowel sound and at last there is silent. length of silence is dependent on length of combination of consonant and vowel. For example if combination ends in 20000th data sample, so the rest of 10000 sample (untill 30000, the length of each sound sample) are silence.   

![alt text](https://github.com/smalekz/PCVC/blob/master/Images/SoundSample.png?raw=true)  

All of sound samples are denoised with "Adaptive noise reduction" algorithm.

Phoneme List in PCVC dataset:
[Here](https://github.com/smalekz/PCVC/blob/master/Images/PhonemeList.JPG)


## How to use
Each files contains just a matrix "x".  
The sign "_N" (N as number) in "Samples" directory (Like in Sample "S0001_2.mat") means this sample is the Nth sample from the speaker of "S0001.mat".
### Matlab
All files are ".mat" files. ".mat" is a fromat for data files in Matlab. Every file consists of a matrix with dimensions 1*23*6*30000 in which 23 is refer to number of consonant, 6 is refer to number of vowel and 30000 is the length of sound sample. order of phonemes are just like shown in [Here](https://github.com/S-Malek/PCVC/blob/master/Images/PhonemeList.JPG). To use it, just open the file and tap on "finish" button to import the data in workspace of Matlab.

### Python
To use ".mat" data files in Python you can use the code below to copy the matrix in the file in "aud" variable (Put your current path instead of "MyPath"). Every file consists of a matrix with dimensions 1*23*6*30000 in which 23 is refer to number of consonant, 6 is refer to number of vowel and 30000 is the length of sound sample. order of phonemes are just like shown in [Here](https://github.com/smalekz/PCVC/blob/master/Images/PhonemeList.JPG).
```
# For example for S1 sample (Reading from source and writing it as "Speaker1.mat" in your current directory):
import urllib.request as urllib2
matfile = urllib2.urlopen("https://raw.githubusercontent.com/S-Malek/PCVC/master/Samples/S0001.mat")
with open('Speaker1.mat','wb') as output:
  output.write(matfile.read())
```
```
# Reading it from current directory and putting the matrix of it in "aud" variable
import scipy.io  
mat = scipy.io.loadmat('Speaker1.mat')  
aud=(mat['x'])
```
### Git
for downloading all together to current directory with git:
```
git clone https://github.com/S-Malek/PCVC
```

## Acknowledgement
So many thanks to those helped us to develop PCVC dataset especially speakers: Farideh Jabraili, Hedayat Malekzadeh, Hamed
Afjuland, Mohammad Ataeizadeh, Tahereh Salari, Alireza Aghaei, Parisa Seyfpour, Sahel Soltani, Mina Bayarash, Milad Abdollahzadeh, Sadra Malekzadeh,...
