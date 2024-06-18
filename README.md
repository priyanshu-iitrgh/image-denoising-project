# image-denoising-project
The code for an image denoising project that is a component of the VLG IITR challenge is available in this repository. The objective is to create a model that can denoise photos efficiently without the need for previously trained models. The experiment findings, assessment metrics, and training code are all included in the repository.
# Data Preparation and Loading
- TensorFlow, NumPy, and other libraries needed for image processing and model creation are imported at the start of the code.
- defines several constants, including MAX_TRAIN_IMAGES, BATCH_SIZE, and IMAGE_SIZE.
- constructs TensorFlow datasets (train_dataset and val_dataset) using tf.data and loads training and validation pictures using glob.Collection
