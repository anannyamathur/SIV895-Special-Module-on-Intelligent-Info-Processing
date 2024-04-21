# Reading Assignment: Deepfakes Detection Using Human Eye Blinking Pattern

## Paper Presented: T. Jung, S. Kim and K. Kim, "DeepVision: Deepfakes Detection Using Human Eye Blinking Pattern," in IEEE Access, vol. 8, pp. 83144-83154, 2020, doi: 10.1109/ACCESS.2020.2988660.

### DATASET:

The dataset is picked from [DeepfakeTIMIT](https://www.idiap.ch/en/scientific-research/data/deepfaketimit), which is a database of videos where faces were swapped using the [open source GAN-based approach](https://github.com/shaoanlu/faceswap-GAN). For this project, 2 real videos, 4 fake videos from the database and 1 fake video of Morgan Freeman from YouTube have been used to test the efficacy of the proposed approach. 

Link to the dataset: [DATASET](https://drive.google.com/drive/folders/1qezSKCqbi2X_SOFHyPpTE1MMt5UEU3WN?usp=drive_link)

### CODE:

The code can be run on Google Colab- [DeepFake Detection Jupyter Notebook](https://colab.research.google.com/github/anannyamathur/SIV895-Special-Module-on-Intelligent-Info-Processing/blob/main/detection.ipynb). The code will automatically load the dataset and the pretrained models ([face landmarks predictor](https://github.com/JeffTrain/selfie/raw/master/shape_predictor_68_face_landmarks.dat )+ [age and gender predictor](https://drive.google.com/drive/folders/1Lb0bRQj-Tdrn5LFy9UjNMfd8r4Tp6UIb?usp=drive_link )) to detect the face landmark points. 

### Results:

The code saw an accuracy of 71.4%. Out of 7 videos, the code could correctly classify 5 videos while it mispredicted one of the fake videos as real and one of the two real videos as fake. In a nutshell, given eye blinking is both an involuntary and voluntary phenomenon, the GAN generated fake videos might have yet not evolved to mimic eye blinking. Though the proposed approach seems to open up a new direction in DeepFake detection, the misprediction of a real video as fake and a fake video as real shows that relying solely on eye blinking is suboptimal. It is yet to be established how gender of a person, activity, time of the day affect eye blinking. In the absence of this, the code pins the predictions on average blink count (17-22 blinks per minute) and average blink period (100-400 ms). 

### References:
- T. Jung, S. Kim and K. Kim, "DeepVision: Deepfakes Detection Using Human Eye Blinking Pattern," in IEEE Access, vol. 8, pp. 83144-83154, 2020, doi: 10.1109/ACCESS.2020.2988660.
- Ranjan, R., Patel, V. M., & Chellappa, R. (2016). HyperFace: A Deep Multi-task Learning Framework for Face Detection, Landmark Localization, Pose Estimation, and Gender Recognition. ArXiv. /abs/1603.01249
- R. Ranjan, V. M. Patel and R. Chellappa, "HyperFace: A deep multi-task learning framework for face detection landmark localization pose estimation and gender recognition" in arXiv:1603.01249, 2016, [online] Available: http://arxiv.org/abs/1603.01249.
- T. Soukupová and J. Cech, "Real-time eye blink detection using facial landmarks", Proc. Comput. Vis. Winter Workshop (CVWW), pp. 42-50, 2016. 
- https://dontrepeatyourself.org/post/how-to-detect-face-landmarks-with-dlib-python-and-opencv/ 

