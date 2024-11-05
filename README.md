# Image classification "in-the-wild"
## Description
The goal of this project is to gather you own real-world image dataset with different types of objects in it and train an image classifier for solving it. Dataset :contaions: shoes, furnitures and books.

## Team info:
* Bata Dániel - B95Q0I
* Bunda Boldizsár - F1LJLQ

## Prerequisutes:
* Docker
* Docker Compose

## Project Structure:
* project_dir
    * Dockerfile
    * docker-compose.yml
    * requirements.txt
    * Data_preparation.ipynb
    * Readme.md

## Usage:
### Clone this repository:
```bash
git clone <repository-url>
cd <project-directory>
```

### Build and run the Docker Container:
```bash
docker-compose up --build
```
Once the container is running, we are be able see the URL in the  terminal that looks like the following:

```bash
http://127.0.0.1:8888/lab?token=<token>
```
Open the URL in a web browser, then open the `.ipynb` file and run the cells in the notebook.

## Notebook contents:
In the `.ipynb` notebook contains the following sections:
* **Data Source**:
    The images are created in-house and saved in a private Hugging Face repository, split into training and test sets. An access token with read-only permission is used to access the repository.
* **Dataset**:
    The dataset is split with an 80:20 ratio, with augmentation applied only to training data to enhance model learning. No further data cleaning is necessary since only a few images are manually verified.
* **Data Processing and Data Module Setup**:
    Images are resized to a resolution of 128x128 pixels with specific transformations applied to training data, such as random zoom and flipping. Validation and test data are processed with consistent resizing and center cropping without random transformations, keeping them "clean" for accurate evaluation.
* **Visualization**:
    A function visualize_images is provided to display random samples from each dataset with the possibility of augmenting training data for visualization.
* **Baseline Models**:
    Two baseline models are created for comparison. The first model randomly selects a class, with an expected accuracy near 33% due to the three classes. The second model always predicts the most common class from the training set, providing a slightly higher accuracy than random guessing.
* **Model Training and Evaluation**:
    The model is set up using a MobileNetV2 architecture modified to classify images into three classes. Training is managed through PyTorch Lightning, with logging to Weights & Biases and early stopping based on validation accuracy. Accuracy and confusion matrix metrics are tracked for performance evaluation, and training and validation accuracy and loss are plotted.

After training, the code plots the accuracy and loss trends for both training and validation sets, enabling performance visualization and identifying potential overfitting or underfitting.
## Stopping the Container:
We are able to stop the container by pressing `Ctrl+C` in the terminal.