# BOTANY 2022 Workshop module 5 - How to train an object classifier

## Training an object classifier
In this module we will learn how to train a simple object classifier, which is a machine learning network capable of assigning a class prediction to an entire image. This type of ML network is useful for many tasks including filtering large datasets and is often one component of more complex software. 

Other types of ML networks can be used for other tasks: object detectors place bounding boxes or polygons around items, semantic segmentation identifies the pixels of an image that correspond to each desired object class, and panoptic segmentation identifies the pixels of an image that correspond to each *instance* of a desired object class and can even learn object associations. 

Here we will train an object classifier to predict the class for a set of rulers that are commonly present in herbarium specimen vouchers. We have a directory filled with rulers that are already grouped into 22 classes including a “fail” class for non-ruler objects. These are our ground truth training data. For this simplicity in this workshop, we will not split our training data into train/validation/test groups, but this is a crucial step of ML development, and it is standard practice to partition annotated data into train/validation/test groups in a roughly 70/15/15 or 60/20/20 ratio. 
# Getting Started
Here is a link to the Colab notebook: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1koHbxPoTn_lGU-Y9upCa_BOI3JuD3Wrj?usp=sharing)

Or use the notebook inside of the module 5 github folder if the link does not work for you. 

As soon as you open the link, make a copy of the notebook in your own account so that you can edit and save any changes to the code.

Please run the first 4 code blocks as soon as you open your copy of the notebook, installing the required packages and downloading the data will take a few minutes.

Once you open the Colab notebook and download the data, you will see three different training datasets: tiny, small, large. For the workshop, please only use the tiny datasets because training on more images will take too much time. We will also need to switch the default CPU runtime in our Colab notebook to a GPU runtime. Using a GPU is ~5 times faster than using a CPU. 

Trained ML networks are also provided if you want to skip the training step.
# Evaluate Model
In the Evaluate Model section, we can choose a trained ML model and see how well it works. You will notice that models that are trained on the larger datasets perform better. Models that are fully trained will outperform models that do not reach a plateau. 
# Running Locally
If you want to modify this code for your own dataset or train it locally, please go to Will Weaver’s GitHub page and clone the “Botany Workshop 2022 - Ruler Classifier” repo: https://github.com/Gene-Weaver/botany-2022-train-object-classifier

There are instructions on setting up a python virtual environment, installing PyTorch, and running the code. 

