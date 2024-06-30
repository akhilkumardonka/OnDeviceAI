# OnDeviceAI

State of the art techniques for deploying models on Edge.

This is my documentation while I was attending the following course by DeepLearning.AI & Qualcommm : [Introduction to on-device AI](https://www.deeplearning.ai/short-courses/introduction-to-on-device-ai/)

## Sphinx Documentation & Deployment on Github Pages

* Create github repo and enable github pages, branched to **gh-pages** and pointing to **/root**.

* Now clone this repo

To build documentation, install sphinx in your python environment and follow below steps:
```
cd <to local repo containing doc folder>
sphinx-build doc _build
```

* Check html page in browser, generated at **/_build.index.html**

* In case of any additional package installations, navigate to below directory : **.github/workflows/documentation.yaml**
and change pip install or sudo apt install commands according to package requirements

* then commit and push repository, github actions will take care of deployments further