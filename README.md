# End-to-End Object Detection for Sign Language Recognition

This project is an **object detection model** designed to recognize and interpret **sign language gestures**. The model is built on **YOLO v5** and fine-tuned to classify six key sign language gestures: 'Hello', 'Yes', 'No', 'Thanks', 'I Love You', and 'Please'. The application allows users to either upload an existing image for sign language detection or activate their camera for real-time recognition.

## Features

- **Image Upload or Live Camera Feed**: Detect sign language from uploaded images or use your camera for live gesture detection.
- **Fine-tuned Model**: Built upon **YOLO v5**, fine-tuned to recognize six important sign language gestures.
- **Custom and Pre-existing Datasets**: The project supports training with either a custom dataset or existing datasets. You can create custom datasets using **Roboflow**.
- **Cloud Storage Integration**: The trained model is pushed to **AWS S3** for scalable cloud storage and retrieval.
- **Pipeline Architecture**: Streamlined processing using a modular pipeline architecture for ingestion, validation, training, and model deployment.
- **Deployment Ready**: Easily deployable on **AWS EC2** using **Jenkins** for CI/CD.

## Project Workflow

The project follows a structured pipeline:

1. **Data Ingestion**: Fetches and processes the dataset for training.
2. **Data Validation**: Ensures the dataset meets the required standards.
3. **Model Training**: Fine-tunes the YOLO v5 model on the provided dataset.
4. **Model Pushing**: Stores the trained model on AWS S3 for easy access.

## Setup Instructions

### Prerequisites

- **Python** 3.7
- **AWS CLI** for cloud storage integration
- **Conda** for environment management

### AWS Setup

1. Install the **AWS CLI** by following [this guide](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html).
2. Configure AWS credentials using the following command:

    ```bash
    aws configure
    ```

   Enter your **AWS Access Key** and **Secret Key** when prompted.
   
3. Create an **S3 bucket** for model storage. The bucket name should match the one specified in your project constants.

### Local Setup

1. Create a new environment and install dependencies:

    ```bash
    conda create -n signlang python=3.7 -y
    conda activate signlang
    pip install -r requirements.txt
    ```

2. Run the application:

    ```bash
    python app.py
    ```

### Project Directory Structure

- **constants**: Contains constants used throughout the project.
- **config_entity**: Defines configuration settings for the project.
- **artifact_entity**: Stores intermediate and final artifacts like the trained model.
- **components**: Implements key components like data ingestion, validation, training, and model pushing.
- **pipeline**: Manages the workflow pipeline for seamless execution of the end-to-end process.
- **app.py**: Main entry point to the application.

### Model Training

This project uses **YOLO v5**, a state-of-the-art object detection model, fine-tuned for recognizing sign language gestures. The training can be performed on both custom datasets and existing datasets, which can be easily created using **Roboflow**.

### Deployment

The project can be deployed to an **AWS EC2 instance** using **Jenkins** for continuous integration and delivery. All necessary configurations and scripts for deployment are included in the project.


### Images

![Screenshot 2024-10-13 152807](https://github.com/user-attachments/assets/4174a29d-ef0c-4f0a-aca4-46f40e009558)





