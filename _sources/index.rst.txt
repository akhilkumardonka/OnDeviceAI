Welcome to Techniques For On Device AI's documentation!
================================================================

This documentation covers the topics dicussed in a newly released course by **deeplearning.ai** & **Qualcomm** i.e. `Introduction to On-Device AI <https://www.deeplearning.ai/short-courses/introduction-to-on-device-ai/>`_. 
I am attempting to present my own perspective and understanding about the topics of the course.

Why On Device AI?
----------------------------

We are all witnessing the rise of AI and its amazing use cases these days. Industry and academia are ensuring that AI models are
easily accessible to end users. This could be done either on Cloud or on the edge. 

Running models on edge offers you several advantages : 

* Cost effective, as we are using local compute
* Reduced latency
* Privacy
* Personalized, based on our needs we can tweak models

On Device AI applications :

* Language models when typing on keyboard, to predict next likely word/sentence
* Images clicked/streaming on mobile app undergoes through several image processing ML models
* Robotics, for understanding and navigating environments
* Voice assistants : for noise suppression & echo cancellation, wake up detection and speech recognition on edge
* Hand writing recognition on keyboards
* Generative AI on edge : live translation, live transcription, photo editing & generation, semantic search, text summarization

Typical Workflow
----------------------------

Models developed after the successful experiments undergoes some necessary engineering to reach end users. This includes :

* Capture model as a computational graph
* Compile above graph for edge device
* Measure real time performance on device
* Metrics validation on target device

Above steps are carried out with device on loop. Once we have carried out and satisfied with edge performance, we can go for 
quantization (**4x faster inference** and **4x smaller model** for low power devices) and final deployment.

Quantization
-----------------

* Two Types

   1. **Weight Quantization** : Where neural network weights are quantized to lower precision
   2. **Activation Quantization** : Where network outputs or activation values are applied with lower precision quantizations

* Available quantizations (weight quant + activation quant) : W8INT8, W8INT16, W4INT16

* Applied in two ways : Post Training Quantization (PTQ), Quantization Aware Training (QAT)

Deployment
-----------------------------

Device integration starts with capturing sensor stream on target device, the GPU preprocessing which involves tensor
restructuring & downsampling, inference through NPU (using runtime APIs) and finally GPU post processing which involves upsampling & thresholding.

We should also package the entire packages properly with all the necessary runtime dependencies (eg. Maven package having 
tflite gpu & npu dependencies).

.. toctree::
   :maxdepth: 2
   :caption: Contents:

   jupyter_notebooks