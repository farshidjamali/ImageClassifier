# ImageClassifier
Custom Image Classifier Using FastAI and Deploying it as an App
references:
1. https://course.fast.ai/
2. https://course.fast.ai/deployment_google_app_engine.html
3. https://medium.com/analytics-vidhya/how-to-create-your-own-custom-image-classifier-and-deploy-it-to-production-5506bb26a74b

In this repository I want to use fast.ai to make my custome image classifier. It is a high-level library build on PyTorch, which allows us to build models using only a few lines of code.

## I will train the model on my own PC, which I have assembled myself and I am proud of!

## Step 1: Downloading Image Data

Search for anything you desire using Google Images. E.g., I want one of my classes to be "Dog" and the other one to be "Cat", therefore I search Dog and scroll down untill enough images are loaded! Now I open the developer console (Hit Ctrl+Shift+J to open your developer console.) for the browser and execute the following two lines of code: 

urls = Array.from(document.querySelectorAll('.rg_di .rg_meta')).map(el=>JSON.parse(el.textContent).ou);
window.open('data:text/csv;charset=utf-8,' + escape(urls.join('\n')));

The links of the image files will get downloaded as a file named download. Then you need to rename the file to dog.txt or name according to your own preference. Then do repeat the above steps for more classes.

Using fast.ai we can get the URLs for the images that we want.

Load and view your data:
Importing libraries
import fastai
fastai.__version__
from fastai import *
from fastai.vision import *


