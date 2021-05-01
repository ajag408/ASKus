# ASKus

## Intro
 - All unprocessed data stored in "data" folder
 - Main Python notebook used to preprocess data/train our model of choice = "ASKus_spaCy.ipynb"

## Info & Adivce/Steps to Run
### Prereqs
1. **You do not need/are not recommended to clone this repo to run it.**  Instead, use a Google Chrome browser and install the "Open in Colab" extension: https://chrome.google.com/webstore/detail/open-in-colab/iogfkhleblhcpcekbiedikdehleodpjo/related.  Once installed, you will see a small, orange infinity icon in the top right of the broswer, next to where the URL is entered.  Click on the notebook in GitHub, then click on this extension to automatically open the notebook in Google Colab
2. After preprocessing our data, the files we were left with were often too bulky to upload to GitHub.  As such, we have stored them all on a Shared Google Drive.  You will need to have access to this shared drive for the code in the notebook to run error-free.  Please email: akash.jagannathan@sjsu.edu, karanbir.bains@sjsu.edu, and/or sudanshushekhar@sjsu.edu to gain access to our Shared Google Drive with preprocessed data and trained models.  We have included cells to mount this drive at the top of the notebook.

### Data Exploration and Preprocessing
3. Scrolling down the notebook, in the Data Exploration and Preprocessing section, you will notice many code cells commented out.  These are preprocessing scripts we used to convert the data into a model-friendly format and to perform a train-test split.  We recommend not uncommenting and running these cells due to the long time needed to execute, however you may do so if you wish.  All necessary files you will need in subsequent sections are already stored on our Shared Google Drive
4. You may run the uncommented cells to see how we pruned our training data

### Model Training
5. There is a script included to train the model, however it takes around 3 hours to complete.  We have already run this and saved the trained model, but you may run it if you wish

### Internal Evaluation
6. We loaded the test data and used our partially trained model to predict dataset labels on a subset of the test data (we could not use the full test data as it took too much computational resources).  We selected 5 random 1% slices of the test data and made predictions on these.  Then, we extracted true positives, false positives, false negatives by comparing our predictions with the ground truth labels and using evaluation metrics defined in the Kaggle competition.  We then used the confusion matrix to extract precision, recall, and the F-score, which is what the competition leaderboard is based on.  
   Runtime for predictions takes approximately 1 hour for the steps described above.  You may see our printed graphs and numbers for our results without having to run it yourself.

### "Restore Test Data to Training Set and Train Model on Full Training Set" Section
6. You can skip this section entirely, as it mimics what was done when training the 70% model above.  We have already saved the fully trained model on our Google Drive

### "Make Predictions on Kaggle Test Data" section
7.  Run this section to see how we used our fully trained model to make dataset label predictions on the test data (4 unseen articles)
