
# Chest Disease Classification Using CT Scan Images

This project focuses on developing a deep learning model to classify various chest diseases using CT scan images. Leveraging convolutional neural networks (CNNs), the model aims to assist in the early detection and diagnosis of chest-related ailments. [Data link](https://drive.google.com/drive/folders/1Z7u504MlagwvzMQH7-X6QZQdsKowTSg8?usp=sharing)

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Chest diseases, such as pneumonia, lung cancer, and tuberculosis, pose significant health challenges worldwide. Early and accurate detection is crucial for effective treatment and improved patient outcomes. Computed Tomography (CT) scans provide detailed images of the chest, making them valuable for diagnosing various conditions. This project utilizes deep learning techniques to automate the classification of chest diseases from CT scan images, aiming to support radiologists and healthcare professionals in diagnostic decision-making.

## Dataset

The dataset comprises labeled CT scan images representing different chest diseases. Each image is categorized into one of several classes, including:

- Normal
- Pneumonia
- Lung Cancer
- Tuberculosis
- COVID-19

The images are preprocessed to ensure uniformity in size and quality, facilitating effective model training.

## Model Architecture

The classification model is built using a Convolutional Neural Network (CNN) architecture, known for its proficiency in image recognition tasks. The architecture includes multiple convolutional layers for feature extraction, followed by fully connected layers for classification. Techniques such as batch normalization and dropout are employed to enhance model performance and prevent overfitting.
## Workflows

1. Update config.yaml
2. Update params.yaml
3. Update the entity
4. Update the configuration manager in src config
5. Update the components
6. Update the pipeline 
7. Update the main.py
8. Update the dvc.yaml 
## Installation

To set up the project locally, follow these steps:

1. **Clone the repository:**

   ```bash
   git clone https://github.com/Tanujkumar24/CHEST-DISEASE-CLASSIFICATON-BY-USING-CT-SCAN-IMAGES.git
   ```

2. **Navigate to the project directory:**

   ```bash
   cd CHEST-DISEASE-CLASSIFICATON-BY-USING-CT-SCAN-IMAGES
   ```

3. **Create and activate a virtual environment (optional but recommended):**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

4. **Install the required dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

## Usage

To train the model with the dataset:

```bash
python main.py --train
```

To evaluate the model on the test dataset:

```bash
python main.py --evaluate
```

For inference on new CT scan images:

```bash
python main.py --predict --image_path path_to_image
```

Ensure that the dataset is properly organized and the paths are correctly set in the configuration file (`params.yaml`) before running the scripts.

### Mlflow dagshub connection uri

```bash
import dagshub
dagshub.init(repo_owner='Tanujkumar24', repo_name='CHEST-DISEASE-CLASSIFICATON-BY-USING-CT-SCAN-IMAGES', mlflow=True)

import mlflow
with mlflow.start_run():
  mlflow.log_param('parameter name', 'value')
  mlflow.log_metric('metric name', 1)

```


### RUN from bash terminal

```bash
export MLFLOW_TRACKING_URI=https://dagshub.com/Tanujkumar24/CHEST-DISEASE-CLASSIFICATON-BY-USING-CT-SCAN-IMAGES.mlflow

export MLFLOW_TRACKING_USERNAME=Tanujkumar24

export MLFLOW_TRACKING_PASSWORD=*****

```



### DVC cmd

1. dvc init
2. dvc repro
3. dvc dag

## Results

The model's performance is evaluated using metrics such as accuracy, precision, recall, and F1-score. Detailed results, including confusion matrices and classification reports, are available in the `results` directory. The model demonstrates high accuracy in classifying chest diseases, indicating its potential utility in clinical settings.

## Contributing

Contributions to enhance the project are welcome. To contribute:

1. Fork the repository.
2. Create a new branch:

   ```bash
   git checkout -b feature-branch
   ```

3. Make your changes and commit them:

   ```bash
   git commit -m "Description of changes"
   ```

4. Push to the branch:

   ```bash
   git push origin feature-branch
   ```

5. Open a pull request detailing your changes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.

---

*Note: This project is for educational and research purposes only. It is not intended for clinical use without further validation.*
