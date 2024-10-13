# Image classification "in-the-wild"
## Description
The goal of this project is to gather you own real-world image dataset with different types of objects in it and train an image classifier for solving it. Our dataset contains the Book, Furniture and Shoe classes.

## Team info:
Team name: Kettőt fizet egyet kap
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
* Data Source:

* Dataset:

* Visualization:

## Stopping the Container:
We are able to stop the container by pressing `Ctrl+C` in the terminal.
