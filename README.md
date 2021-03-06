# DeepMelanomaClassifierApp

The App can be accessed at the following link.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/rooster06/DeepMelanomaClassifierApp/master?urlpath=%2Fvoila%2Frender%2FDeepMelanomaApp.ipynb)

Melanoma is the most serious type of skin cancer, develops in the cells (melanocytes) that produce melanin, early diagnosis is key for recovery.

This web app outputs the probability of Melanoma in images of skin lesions uploaded by the user. The user can also choose the number of Test Time Augmentation (T.T.A.) to get more accurate predictions.

[![Demo Vid](https://github.com/rooster06/DeepMelanomaClassifierApp/blob/master/demo.png)](https://youtu.be/S7FkDImECK0)

<h3>Directions For Use:</h3>

1. Select the desired # of Test Time Augmentations using the slider.
2. Upload an image of the skin lesion you want to check for Melanoma.

<h3>Outputs:</h3>

1. The user, in realtime, will see the test time augmentations being applied and the corresponding model prediction.
2. At the end, The final prediction (avergae of all TTA predictions) is displayed along with the original image uploaded.

<font color='red'>**Note:**</font> This is a proof of concept for research purposes ONLY. Always seek professional medical help in a clinical setting for final diagnosis.



Notes -
- The Inference model in this app is based on the EfficientNet B5 architecture, trained on the SIIM Melanoma dataset.
- The model achieves SOTA performance of 0.9339 AUROC on the test data utilizing heavy Test Time Augmentation, 55 to be exact.
- Feel free to check out the GitHub repo for the scripts and details to train the model.
- The binder docker is sometimes slow, be patient with the App loading or runtime.


Repo Descriptions - 
1. DeepMelanomaApp.ipynb - main driver for the App with widgets 
2. download_gdrive.py - Helper script to download the model weights
3. environment.yml - Docker Environment dependencies and packages setup for app.
4. model.json & yamlmodel.yaml - model architecture as json and yaml files
