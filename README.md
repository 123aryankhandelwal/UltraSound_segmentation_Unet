****

**PROJECT STATEMENT**

Segmentation of Ultrasound(Echocardiographic)Images in different Imagery Planes.

The goal of this project is to provide echocardiographic image segmentation and volume estimation from 2D Ultrasound sequences which consists of both two and four-chamber views.

**DATASET**

The dataset that we are using in our project is the CAMUS dataset.The CAMUS dataset (Cardiac Acquisitions for Multi-structure Ultrasound Segmentation), containing 2D apical four-chamber and two-chamber view sequences acquired from 500 patients.

• CAMUS dataset is a largest publicly-available and fully-annotated dataset for 2D echocardiographic assessment (to our knowledge). 

• Deployment of the segmentation of cardiac structures (left ventricle endocardium and epicardium and left atrium borders).

 • For each patient, there are two corresponding two-chamber (2CH) view acquisition for both End Diastole (ED) and End Systolic (ES) and two       corresponding to the four-chamber (4CH) view acquisition for both End Diastole (ED) and End Systolic (ES).

 •  All results should be saved into a raw/mhd image format. Each segmented image should involve discrete values using the following convention:   

  0 -> background     1 -> left ventricle     2 -> myocardium     3 -> left atrium

![picture](https://github.com/123aryankhandelwal/UltraSound_segmentation_Unet/blob/main/Images/2CH_ED.png)

**OUR APPROACH**

Our first step is the pre-processing of the image and mask.

First, it involves loading of the image file directory to the corresponding data list. 

Pre-processing involves converting of the image from PNG to array using the SimpleITK library.

The last step involves appending of array of images to h5py file for both image and its respective ground truth.

Further, our model is processed and built using U-NET.

##put image

**ARCHITECTURE**

##IMAGE

**OUTPUT** 

Our model is being trained using 50 epochs with 112 steps per epochs. The time taken for training the model per step of epochs is 732s, when trained under Nvidia 1650 GPU. We achieve the loss and accuracy of 0.1098 and 0.9563 for 4CH, 0.0764 and 0.9683 for 2CH.

**2CH OUTPUT IMAGE**



Training and validation loss

##image

Training and validation accuracy

##image



**4CH OUTPUT IMAGE**

Training and validation loss

##image

Training and validation accuracy

##image

**REFERENCE LINKS**









