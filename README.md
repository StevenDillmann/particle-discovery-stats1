# S1 Principles of Data Science Coursework Submission (sd2022)

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

## Description
This project is associated with the submission of the coursework for the S1 Principles of Data Science Module as part of the MPhil in Data Intensive Science at the University of Cambridge. The Coursework Instructions can be found under [Instructions.md](Instructions.md) and the problems to be answered can be found under [DIS\_MPhil\_S1_Coursework\_v2.2.pdf](DIS_MPhil_S1_Coursework_v2.2.pdf). The associated project report can be found under [S1 Coursework Report](report/s1_sd2022_report.pdf).

## Table of Contents
- [Installation and Usage](#installation-and-usage)
- [Support](#support)
- [License](#license)
- [Project Status](#project-status)
- [Authors and Acknowledgment](#authors-and-acknowledgment)

## Installation and Usage

To get started with the code associated with the coursework submission, follow these steps:

### Requirements

- Python 3.9 or higher installed on your system.
- Conda installed (for managing the Python environment).
- Docker (if using containerisation for deployment).

### Steps

You can either run the code locally using a `conda` environment or with a container using Docker. The code is presented in the [s1\_sd2022\_answers.ipynb](src/s1_sd2022_answers.ipynb) Jupyter Notebook (located in the `sd2022/src` directory). The 
notebook will run faster locally on a high-spec computer (recommended).  

#### Local Setup (Using Conda) [RECOMMENDED]

1. **Clone the Repository:**

    Clone the repository to your local machine with the following command:

    ```
    $ git clone https://gitlab.developers.cam.ac.uk/phy/data-intensive-science-mphil/c1_assessment/sd2022
    ```

    or simply download it from [S1 Principles of Data Science Coursework (sd2022)](https://gitlab.developers.cam.ac.uk/phy/data-intensive-science-mphil/s1_assessment/sd2022).

2. **Navigate to the Project Directory:**

    On your local machine, navigate to the project directory with the following command:

    ```
    $ cd /full/path/to/sd2022
    ```

    and replace `/full/path/to/` with the directory on your local machine where the repository lives in.

3. **Setting up the Environment:**

    Set up and activate the `conda` environment with the following command:

    ```
    $ conda env create -f environment.yml
    $ conda activate sd2022_s1_env
    ```

4. **Install ipykernel:**

    To run the notebook cells with `sd2022_s1_env`, install the ipykernel package with the following command:

    ```
    python -m ipykernel install --user --name sd2022_s1_env --display-name "Python (sd2022_s1_env)"
    ```


4. **Open and Run the Notebook:**

    Open the `sd2022` directory with an integrated development environment (IDE), e.g. VSCode or PyCharm, select the kernel associated with the `sd2022_s1_env` environment and run the [s1\_sd2022\_answers.ipynb](src/s1_sd2022_answers.ipynb) Jupyter Notebook (located in the `sd2022/src` directory).


#### Containerised Setup (Using Docker)

1. **Clone the Repository:**

    Clone the repository to your local machine with the following command:

    ```
    $ git clone https://gitlab.developers.cam.ac.uk/phy/data-intensive-science-mphil/c1_assessment/sd2022
    ```

    or simply download it from [S1 Principles of Data Science Coursework (sd2022)](https://gitlab.developers.cam.ac.uk/phy/data-intensive-science-mphil/s1_assessment/sd2022).

2. **Navigate to the Project Directory:**

    On your local machine, navigate to the project directory with the following command:

    ```
    $ cd /full/path/to/sd2022
    ```

    and replace `/full/path/to/` with the directory on your local machine where the repository lives in.

3. **Install and Run Docker:**

    You can install Docker from the official webpage under [Docker Download](https://www.docker.com/).
    Once installed, make sure to run the Docker application.

4. **Build the Docker Image:**

    You can build a Docker image with the following command:

    ```
    $ docker build -t [image] .
    ```

    and replace `[image]` with the name of the image you want to build.

4. **Run a Container from the Image:**

    Once the image is built, you can run a container based on this image:

    ```
    $ docker run -p 8888:8888 [image]
    ```

    This command starts a container from the `[image]` image and maps port `8888` of the container to port `8888` on your local machine. The Jupyter Notebook server within the container will be accessible on JupyterLab at [http://localhost:8888](http://localhost:8888). 

5. **Access and Run the Notebook:**

    After running the container, you'll see logs in the terminal containing a URL with a token. It will look similar to this:

    ```
     http://127.0.0.1:8888/lab?token=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
    ```
    
    Navigate to [http://localhost:8888](http://localhost:8888) and enter the token `XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX`. Once you accessed JupyterLab, run the [s1\_sd2022\_answers.ipynb](src/s1_sd2022_answers.ipynb) Jupyter Notebook (located in the `sd2022/src` directory) with an `ipykernel` (Python 3).

    **Note:** Make sure that not other Jupter Notebook Servers are running. Otherwise, you might encounter 'Invalid credentials' issues when entering the token. Close any running Jupter Notebook Servers. To stop a running server, use `Ctrl + C` in the terminal where you launched JupyterLab. Also make sure port `8888` is not occupied.


## Support
For any questions, feedback, or assistance, please feel free to reach out via email at [sd2022@cam.ac.uk](sd2022@cam.ac.uk).

## License
This project is licensed under the [MIT License](https://opensource.org/license/mit/) - see the [LICENSE](LICENSE) file for details.

## Project Status
The project is in a state ready for submission. All essential features have been implemented, and the codebase is stable. Future updates may focus on minor improvements, bug fixes, or optimisations.

## Note on the Use of auto-generation tools
GitHub Co-Pilot assisted the author in producing all function docstrings present in the project repository. No specific commands have been given, instead auto-completion suggestions have occasionally been accepted.

## Authors and Acknowledgment
This project is maintained by [Steven Dillmann](https://www.linkedin.com/in/stevendillmann/) at the University of Cambridge.

17th December 2023

