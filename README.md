Skin Cancer Detection using Logistic Regression and SVM

Overview

This project aims to develop a machine learning model to detect skin cancer from images using Logistic Regression and Support Vector Machines (SVM). The goal is to build a reliable and efficient classifier that can distinguish between benign and malignant skin lesions, aiding in early diagnosis and treatment.

Table of Contents

- Installation
- Dataset
- Preprocessing
- Model Training
- Evaluation
- Usage
- Contributing
- License

 Installation

To run this project locally, you need to have Python installed. We recommend using a virtual environment to manage dependencies. Follow these steps:

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/skin-cancer-detection.git
   cd skin-cancer-detection
   ```

2. Create and activate a virtual environment:
   ```sh
   python -m venv venv
   source venv/bin/activate   # On Windows use `venv\Scripts\activate`
   ```

3. Install the required packages:
   ```sh
   pip install -r requirements.txt
   ```

Dataset

The dataset used in this project is the [ISIC Skin Cancer Detection dataset](https://challenge2017.isic-archive.com/). You need to download the dataset and place it in the `data` directory.

- Structure of the `data` directory:
  ```
  data/
  ├── train/
  │   ├── benign/
  │   └── malignant/
  └── test/
      ├── benign/
      └── malignant/
  ```

Preprocessing

The preprocessing steps include:

1. Resizing Images: All images are resized to a standard size for uniformity.
2. Normalization: Pixel values are normalized to a range of [0, 1].
3. Data Augmentation: Techniques like rotation, flipping, and scaling are applied to augment the training data.

Run the preprocessing script:
```sh
python preprocess.py
```

 Model Training

Two models are trained in this project:

1. **Logistic Regression**
2. **Support Vector Machine (SVM)**

To train the models, run:
```sh
python train.py --model logistic_regression
python train.py --model svm
```

 Evaluation

The trained models are evaluated using various metrics like accuracy, precision, recall, and F1-score. To evaluate the models, run:
```sh
python evaluate.py --model logistic_regression
python evaluate.py --model svm
```

 Usage

After training and evaluating the models, you can use them to make predictions on new images. Run the prediction script as follows:
```sh
python predict.py --model logistic_regression --image path/to/image.jpg
python predict.py --model svm --image path/to/image.jpg
```

 Contributing

Contributions are welcome! Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch: `git checkout -b my-feature-branch`.
3. Make your changes and commit them: `git commit -m 'Add some feature'`.
4. Push to the branch: `git push origin my-feature-branch`.
5. Submit a pull request.


Feel free to open an issue if you have any questions or run into any problems.
