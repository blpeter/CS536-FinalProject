# CS536 Final Project: Referring Expressions with CLIP and SAM
Welcome to the repository for my CS536 final project. Below are directions about how to run the code and some information about each file. This project creates four different models that test the accuracy of object detection using referring expressions. The PDF document provides detailed information about each of the models. 

# Setting up your Environment
Note: This code and setup were tested on Ubuntu 20.04.4 LTS. It should work on other Linux distros, but it was not tested for compatibility. All of the commands were run in the terminal using a bash shell.

Steps to reproduce the results:

1. Install Anaconda: https://docs.anaconda.com/free/anaconda/install/linux/
2. Verify you can access conda commands such as 'conda --version'.
3. Clone this repo into a directory of your choice.
4. After finishing cloning, enter the directory you cloned to so you can see the files as shown in the repository.
5. Create a new Python environment by running the following command: 'conda env create -f environment.yml'
6. Activate your new environment by running this command: 'conda activate RefwSAM'
7. Download the refCOCO dataset with this command: 'bash download_coco.sh' (this will take a while).
8. Downlaod the SAM modle checkpoint here: https://dl.fbaipublicfiles.com/segment_anything/sam_vit_h_4b8939.pth. From the command line you can run 'wget https://dl.fbaipublicfiles.com/segment_anything/sam_vit_h_4b8939.pth'. Place it in the same directory as the notebook files.
9. Once the refCOCO data set is complete, launch jupytr-notebook. From the command line, this is done by running 'jupyter-notebook'.
10. Start by opening baseline.ipynb and running it from the beginning. If this notebook completes successfully, all other notebooks should run.

These notebooks can take a while to run, but there are progress bars for the long-running sections that will show you the status. 

# Description of each Notebook

baseline.ipynb: This is the basecase that we used to compare to the other models. Uses SAM, CLIP, and position features.

Large_Image.ipynb: This is the large image model. This uses SAM and CLIP with no sub-image or position features. 

Small_Image.ipynb: This is one of the sub-image models. Uses SAM, CLIP, and position features.

Small_Image-NoPos.ipynb: This is one of the sub-image models. Uses SAM and CLIP.

SAM_test.ipynb: This notebook was used to test features of the SAM ViT.
