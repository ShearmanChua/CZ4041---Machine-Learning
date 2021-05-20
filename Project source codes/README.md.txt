# CZ4041-Machine-Learning Course Project

===================================================================================
         Converting Dog Breed Identification Kaggle Dataset to TFRecords
===================================================================================

In order to utilize the TPU hardware accelerator in Google Colaboratory when training the Dog Breed Identification classification model, we will require to convert the labels and images from the Dog Breed Identification Kaggle Dataset into TFRecords format, as it is impossible to use the Cloud TPUs unless you can feed them data quickly enough using the tf.data.Dataset API. We will be using the tf.data API for reading and writing data in TensorFlow.

The python notebooks to convert the Dog Breed Identification Kaggle Dataset into TFRecords and store them onto our Group's Google Cloud Storage are available publicly
on Kaggle at the following links:

Converting Train Dataset into TFRecords:

https://www.kaggle.com/shearmanchua/create-tfrecords-for-dog-breed-classification

Converting Test Dataset into TFRecords:

https://www.kaggle.com/shearmanchua/test-tfrecords

### Step 1: To run both the Python notebooks to convert the Dog Breed Identification Kaggle Dataset into TFRecords, you will first need to ensure that the datasets required are loaded during runtime. If any of the dataset is not loaded, you can do so by selecting the "+ Add data" button at the top right hand corner of the Kaggle notebook environment and search for the "dog breed identification" Kaggle competition 
dataset.

For the credentials for the Google Cloud storage, you can download the credentials .json file using the following link:

www.kaggle.com/dataset/98f0f0d20976250c447d13f3638be0d05e23f681246e18c7a12055732c62d2b9

and then upload it to the Kaggle notebook environment by selecting the "+ Add data" button at the top right hand corner of the Kaggle notebook environment and click the "Upload" button 

### Step 2: Run all the cells in the Kaggle notebooks and the TFRecords will be created and uploaded into the Google Cloud Platform buckets

===================================================================================
         Running the Google Colab Notebooks for Classification
===================================================================================

For the Final Classfication Model Used to obtain our final Dog Breed Identification Kaggle Competition Leaderboard score, it can be found in the submission folder. The 
attached notebook can be run on Google Colab as well as from the link below:

https://colab.research.google.com/drive/1QWOo5ur3YHbCTTvJZP8zBED_IAem2Wba?usp=sharing

### Step 1:Upload the "CZ4041 Final Classification Model.ipynb" notebook to drive and open it with google colab.

To run the notebooks, we will need TPU hardware accelerator as well as the built-in environment of google colab. Therefore, rather than running on the local machine, using google colab to execute these notebooks is recommended.

### STEP 2: Change the runtime type of google colab notebook to "TPU".
Go to Runtime > Change runtime type. \
Under Hardware Accelerator, select "TPU"

### STEP 3: Upload the "labels.csv" file to the Google Colab Environment by selecting the "Files" icon at the top left of the Google Colab Environment and dragging the "labels.csv" file to the expanded "Files" column.

### STEP 4: Run the "CZ4041 Final Classification Model.ipynb" notebook sequentially until the text cell titled "Predict on Test Set from Kaggle", making sure to follow the links to insert the credentials for the "Mount google Drive" and "authenticate Google credentials" cells. There are commented cells that have specific instructions for running them within the cells. Those commented cells are cells to save the images and trained model to the Google Drive mounted as well as to load the saved train model from the mounted Google Drive. Uncomment them if you want to save the images and trained classification model.

### NOTE: If you would like to load the final trained model that our team has trained, it can be found at the following link:

https://drive.google.com/drive/folders/1ltYu1_YlU-LqUcCM0u5aP9GiM9g_BL8I?usp=sharing

### STEP 5: In order to run the predictions on the test set from Kaggle using the trained model, when reached the "Load class mapping from CSV file" section, upload the "classes_mapping.csv" file to the Google Colab Environment by selecting the "Files" icon at the top left of the Google Colab Environment and dragging the "classes_mapping.csv" file to the expanded "Files" column. This is to retrieve the class mappings we have made earlier when creating the TFRecords to change the 120 Dog Breed Classes to integers. 

### STEP 6: In order to generate the predictions csv file, when reached the "Load Sample Submission csv" section, upload the "sample_submission.csv" file to the Google Colab Environment by selecting the "Files" icon at the top left of the Google Colab Environment and dragging the "sample_submission.csv" file to the expanded "Files" column.

### STEP 7: Run the remaining cells to generate the predictions CSV file for uploading to Kaggle. When reached the "Save predicitions results to CSV" section, change the file path to save the CSV file to the file path you want to save the CSV file to for your mounted Google Drive


### Note: If you would like to check the TFRecords used for the Training and validation datasets, you can view them using the following links:

Training TFRecords:

https://console.cloud.google.com/storage/browser/cz4041_train_10;tab=objects?forceOnBucketsSortingFiltering=false&authuser=4&project=loyal-column-305212&supportedpurview=project&prefix=&forceOnObjectsSortingFiltering=false

Validation TFRecords:

https://console.cloud.google.com/storage/browser/cz4041_val_10;tab=objects?forceOnBucketsSortingFiltering=false&authuser=4&project=loyal-column-305212&supportedpurview=project&prefix=&forceOnObjectsSortingFiltering=false

Our team's final .csv file of our model's prediction results submitted to Kaggle can be found in the .csv file "prediction results.csv" in the submission folder

===================================================================================
                               Additional Final Notes
===================================================================================

Although our team's final classification model found in the "CZ4041 Final Classification Model.ipynb" notebook does not make use of additional data, as mentioned in the Course assignment report, our team trained additional classification models which made use of additional data in order to determine if the inclusion of additional data found from Flickr improves the performance of the models. The additional data used can be found in the Github link as follow:

https://github.com/ShearmanChua/CZ4041---Machine-Learning/tree/main/new_labels

The Kaggle notebook used to append the additional data to our Google Cloud Storage and transform them into TFRecords can be found using the following link:

https://www.kaggle.com/shearmanchua/append-more-training-data-to-tfrecords

The python notebooks used to obtain the additional dog images from Flickr, with the readme file are contained in the Google Drive Folder with the following link:

https://drive.google.com/drive/folders/1iT2qRm3MKA7U6IS_Krk5Pj9yc8jN9kdJ?usp=sharing

