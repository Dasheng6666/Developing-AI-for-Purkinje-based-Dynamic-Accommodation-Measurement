Following-up plans for AI-based Modeling for Purkinje-based Dynamic Accommodation Measurement
________________________________________
1. Background and Motivation
In my opinion, Purkinje-image–based measurement does provide a compact and optically efficient solution for estimating dynamic ocular accommodation in smart glass systems. Recent work demonstrated that accurate measurement of human eye dynamic accommodation and binocular convergence is achieved by combining Purkinje reflections with machine learning (MLP) to some extent.
We plan to extend that work with 3 perspectives, including developing AI algorithms for calibration, data training, and analysis in a smart glass system
________________________________________
2. Plan and procedure
To be more specific and guiding, my rough plans are:
The main objectives are:
•	For data training and improving robustness, In the data acquisition and preprocessing stage, image segmentation and feature extraction are used to denoise and normalize pupillary and Purkinje-related features, (like illumination changes, blinking, head motion). During model training, split training and test dataset. grid search, dropout, and data augmentation are applied to optimize the MLP, and increasing data diversity with accurate labeling improves the model’s generalization and robustness (maybe leave-one-subject-out (LOSO) protocol or introduced to learn subject-specific scale and bias parameters)
•	For calibration, we implement a user-specific multi-point calibration procedure (For example, use least squares regression to learn the offset for each user) that learns a linear compensation model from known accommodation targets to correct MLP predictions, or many be best ML structure like CNN and RNN
•	Also, Model performance is evaluated using cross-validation and subject-independent testing to analyze generalization across users and systematically evaluate robustness, latency, and generalization under realistic smart-glass constraints.
________________________________________
3. Expected Outcomes
•	Improved dynamic accuracy and smoothness of accommodation estimation.
•	Reduced calibration error under minimal calibration effort.
•	A unified AI framework suitable for real-time smart-glass deployment.

