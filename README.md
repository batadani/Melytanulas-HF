# Image classification "in-the-wild"
## Description
The goal of our project is to gather our own real-world image dataset with different types of objects in it and train an image classifier for solving it. Our dataset contains the Book, Furniture and Shoe classes.

## Team info:
Team name: Kettőt fizet egyet kap
* Bata Dániel - B95Q0I
* Bunda Boldizsár - F1LJLQ

## Prerequisutes:
* Docker
* Docker Compose

## Project Structure:
* project_dir
    * Dockerfile: This file specifies which base image to use, which dependencies to install, and how to configure the application.
    * docker-compose.yml: The docker-compose.yml file allows for the management and configuration of multiple Docker containers together. With this file, we can define the different services of our application (e.g., web server, database) and specify how they should communicate with each other.
    * requirements.txt: The requirements.txt file contains the Python packages and their versions that the application uses. This file is used by the pip package manager to install dependencies.
    * Data_preparation.ipynb: Notebook file running the aquisition and preparation of our data, along with showing analysis of our data's composition.
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
### Data Source:
Shows that the images we use are stored in a huggingface repository the way of importing them, and shows the current image counts of the different classes.
### Dataset:
Loads the images into a DataModule that augments the training images to later improve training while keeping valuation and testing data unaugmented, all cropped to a uniform size.
### Visualization:
Shows some examples of what images and augments the CNN will use later on.

## Stopping the Container:
We are able to stop the container by pressing `Ctrl+C` in the terminal.
