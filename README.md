# Image-denoising-project
The code for an image denoising project that is a component of the VLG IITR challenge is available in this repository. The objective is to create a model that can denoise photos efficiently without the need for previously trained models. The experiment findings, assessment metrics, and training code are all included in the repository.
# Data Preparation and Loading
- TensorFlow, NumPy, and other libraries needed for image processing and model creation are imported at the start of the code.
- defines several constants, including MAX_TRAIN_IMAGES, BATCH_SIZE, and IMAGE_SIZE.
- constructs TensorFlow datasets (train_dataset and val_dataset) using tf.data and loads training and validation pictures using glob.Collection

# Model Architecture (ZeroDCE class and build_dce_net)
- Uses the Keras API provided by TensorFlow to define the architecture of the DCE (Denoising and Contrast Enhancement) network.
- A sequence of convolutional layers with skip connections is built using the build_dce_net() function.
- Keras extends the ZeroDCE class.Model and has functions for calculating losses (compute_losses), enhancing images (get_enhanced_image and call), creating custom training (train_step), evaluating the model (test_step), and compiling the model.includes specially designed loss algorithms for denoising and contrast enhancement applications (colour consistency loss, exposure loss, illumination smoothness loss, and spatial consistency loss).
# Training the Model
- Compiles the ZeroDCE model with an Adam optimizer and custom loss functions.
- Fits the model to train_dataset for a specified number of epochs (100 in this case) while validating on val_dataset.
- The training history (history) is stored to track loss metrics over epochs.
# Evaluation and Visualization
Defines utility functions (plot_result) to visualize training and validation losses over epochs using matplotlib. Includes functions to plot images (plot_result) for visual comparison of original, autocontrast, and enhanced images.
# PSNR Calculation
PSNR stands for Peak Signal-to-Noise Ratio, and it is a metric used to quantify the quality of an image or signal after it has been processed or compressed compared to an original, uncompressed version. In other words PSNR is a quality metric commonly used in image processing tasks to quantify the difference between two images.

#
