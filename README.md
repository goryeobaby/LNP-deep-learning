This repository features Python scripts and Jupyter notebooks to support the study:

**Deep learning models for lipid-nanoparticle-based drug delivery**

*Note: The LNP data used in the scripts and notebooks is not included in this repository*, but can be found at https://scilifelab.figshare.com/articles/LNP_drug_delivery_image_data/12482183/1

Owned by: goryeobaby

Within this repository, you will find several primary notebooks and scripts:

**1. LNP_CNN_data_prep.ipynb**
Data preparation to extract cell-level time-lapse data needed for the CNNs.

**2. LNP_CNN_train.ipynb**
Training the CNN between time points 1 and 20 in two prediction models (classification and regression) and performing 5-fold cross-validation.

**3. LNP_time-series_data_prep.ipynb**
Using the trained CNNs create the time-series data required for the LSTM and tsfresh based applications.

**4. LNP_LSTM_model_selection.ipynb**
200 sample grid search for finding the best LSTM model architecture for each prediction mode and cross-validation fold.

**5. LNP_LSTM_train.ipynb**
Train the best LSTM models from the model selection and save out predictions on the test set.

**6. LNP_tsfresh_efficient_extract_select_PCA.py**
Using tsfresh with the efficient parameters setting to extract and select the relevant time-series features, followed by PCA for dimension reduction.

**7. LNP_tsfresh_efficient_gbm.ipynb**
Gradient boosting machine (GBM) grid search based on the time series features derived from (6), and save out predictions on the tests set from the best GBM model.