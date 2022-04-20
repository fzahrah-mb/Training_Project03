# Convolutional Neural Network for Concrete Crack Images for Classification
_Using a Convolutional Neural Network and applied Transfer Learning for Concrete Crack Images for Classification_

## Description

- The model utilises the [Concrete Crack Images for Classification Dataset from Mendeley Data][df1] to classify concrete crack images wether they are indeed a crack or otherwise.
- In a summary, the data set are required from he data is collected from various METU Campus Buildings.
- A Convolutional Neural Network and applied Transfer Learning is used for the project because of the relatively high number of the images, exactly 40,000 images (positive & negative) in total.

## Methodology
#### The project can be divided into several sections:
- Data Acquisition
    - Since the project is configured in Google Colab, the zipped file of the images are stored in the Google Drive, instead of uploading all of the  40,000 images directly to it.
    - The first 2 lines of the syntax are used to perform the extraction of the zipped files into the Google Colab, which takes much less time then uploading alll of the images.
- Data Set Definition
    - The images are already stored in either "Positive"; for a definite crack images or "Negative"; not crack images in the zipped files.
    - The data set are only defined as in which images will be in the train, validation or test dataset.
- Data Configuration
    - tf.data builds a performance model of the input pipeline and runs an optimization algorithm to find a good allocation of its CPU budget across all parameters specified as AUTOTUNE. While the input pipeline is running, tf.data tracks the time spent in each operation, so that these times can be fed into the optimization algorithm.
- Model Definition from Transfer Learning
    - The project has applied Transfer Learning from MobileNetV2 as the base model. MobileNetV2 is chose because it is a relatively lightweight model but still delivers an acceptable model accuracy
- Model Modification
    - Some modifications are made at the end of the base model to complete it:
        - Addition of 1 pooling layer.
        - Addition of 1 dense output layer.
- Model Training
- Model Evaluation

## Results
- The training was set to run for 10 epochs only due to the huge amount of time take to complete an epoch.
- Model evaluation was done after model training and the results are:
    - Test loss = 0.01
    - Test accuracy = 0.99

## License
Copyright (c) [2022] [Fatimah Zahrah binti Mohd Badry]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
MIT

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [df1]: <https://data.mendeley.com/datasets/5y9wdsg2zt/2>