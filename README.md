# KSP-IPH2019-Table39
Age is just a number(Facial recognition)

# Project Synopsis:
Solving cases of missing people are hard as more years pass because as we age, our face structure changes. Facial recognition is almost impossible here. To combat this, we suggest creating an aged data set from our existing data set of missing subject cases using Generative Adversarial Networks. By simulating aging, we can then compare any photo taken on sighting with this aged data set. If we know the approximate age, we can check only that subset of the aged data setelse we can runa search through the entire aged data set. This we can recognize subjects real-time whether they have been missing for a few days, or for many years.

# List of tools:
Google Colab
Python 3, Runtime - GPU

# Steps followed(Code with output):
# For facial recognition
Step 1.
There are three known databases - Arrested, Wanted, Dead
Deposit all folders into a single folder known_images by running merging.ipynb

Step 2.
We need to search known_images and identify missing_images by running FR.ipnyb
The known and unknown encoding data(specific facial features) are uploaded in a csv file.

# For aging
Step 3.
We divide the missing_images into folders according to their age, referencing the metadata, by running folders_for_police.ipynb

Step 4.
We proprocess by running preproc.ipynb for each folder. This identifies faces, isolates, crops, resizes to (128,128), and greyscale.
The process is depicted in the screenshot preproc_op.jpeg.

