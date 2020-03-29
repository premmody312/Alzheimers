# Alzheimers
Alzheimer's Disease can be detected using this Deep Learning Engine

## Work done in brief:

The following exploratory analysis will be concerned with diagnosing patients as AD or NC
using CNN. The data consisting of T1-weighted coronal brain MRI scans and the corresponding table of patient information come from the Open Access Series of Imaging Studies (OASIS): Cross-sectional MRI Data in Young, Middle Aged,Non-demented, and Demented Older Adults .  
       
After removing, NaN values and patients who did not have a CDR score, the number of patients reduced to 216 from 416.Each patient had 10 coronal slices from slice in total making 2160 images. Patient 58 is a representative NC patient, since she is 46 years old and has a CDR score of 0. Patient 308 is a representative AD patient, since she is 78 years old, and has a CDR score of 2.
      
Using the Open-CV module, the image was read in as a three-dimensional numpy array of size 176x176x3, where 3 corresponds to the 3 red, green, and blue (RGB) channels. This was then normalized by dividing each intensity by 255, the maximum intensity. What may be novel about this study, regarding AD diagnosis, is the following preprocessing step of running K-Means clustering algorithm on the pixel values.
      
The 2160 images were then partitioned into a training set and a validation set, where 70% of the 2160 images, or 1512 images, were used to train the model in folds or batches, while the other 30%, or 648 images, were used to validate the model.Each epoch took about 30 seconds to train with the default learning rate on stochastic gradient descent at 0.01. Over a 150 epochs, training took approximately 60 minutes or almost 1 hour.
     
Thus we were able to obtain an accuracy of  84.41% by applying K-Means for Pre-Processing Images before using Convolution Neural Networks and then using Canny Edge Detection Algorithm. In conclusion, the model of preprocessing with k -means and training performed well (training accuracy = 100%, prediction accuracy = 84.41%, AUC = 0.904).   

## Resources / Tools used:

OpenCV,Tensorflow,Keras(Python)

## Key learnings from the internship:

Computer Vision and Deep Learning

## Conclusion:

Thus, Alzheimer's Disease Detection as a project was completed and we successfully learned Computer Vision and Deep Learning.
