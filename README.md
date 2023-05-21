# Face Recognition README

This project is a face recognition system that can identify faces in images and videos. It uses machine learning techniques to train a model on a set of labeled face images and then uses that model to recognize faces in test images and videos.

## Installation

### Windows

1. Install Visual Studio:
   - Download and install Visual Studio from the official website: [https://visualstudio.microsoft.com/](https://visualstudio.microsoft.com/)
   - During the installation, make sure to select the option to install C++ support.

2. Install Boost:
   - Download the Boost library from the Boost website: [https://www.boost.org/](https://www.boost.org/)
   - Extract the downloaded Boost library to a local directory.

3. Install required Python packages:
   - Open a command prompt and navigate to the project directory.
   - Run the following command to install the required packages:
     ```
     pip install --upgrade pip
     pip install scikit-learn matplotlib tqdm opencv-python dlib
     ```

4. Download the shape predictor file:
   - Download the shape predictor file (`shape_predictor_68_face_landmarks.dat`) from the dlib website: [http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2](http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2)
   - Extract the downloaded file and place it in the project directory.

5. Run the project:
   - Modify the code in the project files as needed for your specific use case.
   - Run the main script to start the face recognition system.

### macOS

1. Install Xcode:
   - Install Xcode from the App Store.
   - Open Xcode and follow the instructions to install the required components.

2. Install Boost:
   - Open a terminal and run the following command to install Homebrew if you haven't already:
     ```
     /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
     ```
   - Run the following command to install Boost using Homebrew:
     ```
     brew install boost
     ```

3. Install required Python packages:
   - Open a terminal and navigate to the project directory.
   - Run the following command to install the required packages:
     ```
     pip install --upgrade pip
     pip install scikit-learn matplotlib tqdm opencv-python dlib
     ```

4. Download the shape predictor file:
   - Download the shape predictor file (`shape_predictor_68_face_landmarks.dat`) from the dlib website: [http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2](http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2)
   - Extract the downloaded file and place it in the project directory.

5. Run the project:
   - Modify the code in the project files as needed for your specific use case.
   - Run the main script to start the face recognition system.

### Ubuntu

1. Install Boost:
   - Open a terminal and run the following command to install Boost:
     ```
     sudo apt-get install libboost-all-dev
     ```

2. Install required Python packages:
   - Open a terminal and navigate to the project directory.
   - Run the following command to install the required packages:
     ```
     pip install --upgrade pip
     pip install scikit-learn matplotlib tqdm opencv-python dlib
     ```

3. Download the shape predictor file:
   - Download the shape predictor file (`shape_predictor_68_face_landmarks.dat`) from the dlib website: [http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2](http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2)
   - Extract the downloaded file and place it in the project directory.

4. Run the project:
   - Modify the code in the project files as needed for your specific use case.
   - Run the main script to start the face recognition system.

## Usage

1. Prepare the training data:
   - Create a directory to store the training images.
   - Organize the images into subdirectories, where each subdirectory represents a person and contains their face images.
   - Update the `train_dir` variable in the code to point to the directory containing the training images.

2. Train the model:
   - Run the script to extract facial features from the training images and train the SVM classifier.
   - The trained model will be stored in memory for subsequent use.

3. Test images:
   - Place the test images in a separate directory.
   - Update the `test_dir` variable in the code to point to the directory containing the test images.
   - Run the script to identify faces in the test images.
   - The identified images will be moved to the `output/images` directory, organized by the predicted labels.

4. Test videos:
   - Place the test videos in a separate directory.
   - Update the `test_dir` variable in the code to point to the directory containing the test videos.
   - Run the script to identify faces in the test videos.
   - The identified videos will be moved to the `output/videos` directory, organized by the predicted labels.


## Improvements
The face recognition system provided in this project serves as a basic implementation. Here are some potential areas for improvement:

1. ### Data Augmentation: 
    - Consider applying data augmentation techniques such as rotation, scaling, and flipping to increase the diversity of the training data. This can help improve the robustness and generalization of the model.

2. ### Hyperparameter Tuning:
    - Experiment with different hyperparameters for the SVM classifier, such as the kernel type, regularization parameter, and gamma value. Grid search or other optimization methods can be used to find the best combination of hyperparameters for improved performance.

3. ### Feature Selection/Extraction: 
    - Explore alternative methods for feature selection or extraction. Dlib's 68 facial landmarks are used in this project, but there are other feature extraction techniques, such as deep learning-based methods, that may yield better results.

4. ### Ensemble Methods: 
    - Investigate ensemble methods, such as bagging or boosting, to combine multiple classifiers for improved accuracy and robustness.

5. ### Real-time Face Recognition: 
    - Extend the system to perform real-time face recognition using live video streams. This can involve optimizing the code for efficient video processing and integrating with appropriate libraries or frameworks.

6. ### Error Analysis: 
    - Analyze the errors made by the model and identify common patterns or challenging scenarios. This can provide insights into areas where the model may be failing and guide further improvements.

7. ### User Interface:
    - Develop a user-friendly interface to interact with the face recognition system, allowing users to easily add new training images, perform recognition on custom datasets, and visualize the results.

These are just a few potential avenues for improvement. Feel free to explore and experiment with different techniques and approaches to enhance the face recognition system.

If you make any improvements or have suggestions, contributions to this project are highly encouraged. Please refer to the "Contributing" section for more information.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more information.

## Acknowledgments

This project uses the following libraries:
- scikit-learn: [https://scikit-learn.org/](https://scikit-learn.org/)
- matplotlib: [https://matplotlib.org/](https://matplotlib.org/)
- tqdm: [https://tqdm.github.io/](https://tqdm.github.io/)
- OpenCV: [https://opencv.org/](https://opencv.org/)
- dlib: [http://dlib.net/](http://dlib.net/)

## Contributing

Contributions are welcome! Please feel free to open a pull request or submit an issue if you find any problems or have suggestions for improvements.