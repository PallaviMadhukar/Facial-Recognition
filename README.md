# KSP-IPH2019-Table39
Indian Police Hackathon '19
Topic: Facial Recognition
Team Name: Age is just a number

# Project Synopsis:
Solving cases of missing people are hard as more years pass because as we age, our face structure changes. Facial recognition is almost impossible here. To combat this, we suggest creating an aged data set from our existing data set of missing subject cases using Generative Adversarial Networks. By simulating aging, we can then compare any photo taken on sighting with this aged data set. If we know the approximate age, we can check only that subset of the aged data set else we can run a search through the entire aged data set. This we can recognize subjects real-time whether they have been missing for a few days, or for many years.

# List of tools:
Google Colab
Python 3, Runtime - GPU

# Steps followed(Code with output):
## For facial recognition
To prove that there is requirement of aging in facial recognition, we have uploaded Proof.ipynb. Here we can see that a younger version of a person does not match the same person after a few years because of changes in the facial structure.

Step 1.
There are three known databases - Arrested, Wanted, Dead
Deposit all folders into a single folder known_images by running merging.ipynb

Step 2.
We need to search known_images and identify missing_images by running FR.ipnyb
The known and unknown encoding data(specific facial features) are uploaded in a csv file.

## For aging
Step 3.
We divide the missing_images into folders according to their age, referencing the metadata, by running folders_for_police.ipynb. The result is police_db1.zip.

Step 4.
We proprocess by running preproc.ipynb for each folder. This identifies faces, isolates, crops, resizes to (128,128), and greyscale.
The process is depicted in the screenshot preproc_op.jpeg.

Step 5.
We train the images by running Training_Final.ipynb. The resultant output after every epoch is shown in trials_training_op.jpeg

Step 6. 
We form a new database by running the trained model on Testing.ipynb.This ages missing_images and each image is aged and deposited into the respective age folder. Thus we get a copy of the aged image in every age folder.

Apart from doing this with the missing_images, we also validating this with a celebrity database UTKFace. We segregated only Indians to get a refined output and this folder is zipped and uploaded as aged_celeb_ds.zip.

Step 7.
When we input an image of a person who we think may be missing, their gender and approximate age, it is compared to the subset of aged data set. If there is a match, the image is that of a missing person. 

# Result
Our matches are uploaded in Matches.xlsx



