# OpenCV
OpenCV Demos

# Configure and Manage Your Environment with Anaconda
Per the Anaconda docs:

Conda is an open source package management system and environment management system for installing multiple versions of software packages and their dependencies and switching easily between them. It works on Linux, OS X and Windows, and was created for Python programs but can package and distribute any software.

# Overview
Using Anaconda consists of the following:

Install miniconda on your computer, by selecting the latest Python version for your operating system. If you already have conda or miniconda installed, you should be able to skip this step and move on to step 2.
Create and activate * a new conda environment.
* Each time you wish to work on any exercises, activate your conda environment!

# 1. Installation
Download the latest version of miniconda that matches your system.

NOTE: There have been reports of issues creating an environment using miniconda v4.3.13. If it gives you issues try versions 4.3.11 or 4.2.12 from here.

# Linux	Mac	Windows
64-bit	64-bit (bash installer)	64-bit (bash installer)	64-bit (exe installer)
32-bit	32-bit (bash installer)		32-bit (exe installer)
Install miniconda on your machine. Detailed instructions:

Linux: http://conda.pydata.org/docs/install/quick.html#linux-miniconda-install
Mac: http://conda.pydata.org/docs/install/quick.html#os-x-miniconda-install
Windows: http://conda.pydata.org/docs/install/quick.html#windows-miniconda-install
2. Create and Activate the Environment
For Windows users, these following commands need to be executed from the Anaconda prompt as opposed to a Windows terminal window. For Mac, a normal terminal window will work.

# Git and version control
These instructions also assume you have git installed for working with Github from a terminal window, but if you do not, you can download that first with the command:

# conda install git
If you'd like to learn more about version control and using git from the command line, take a look at our free course: Version Control with Git.

Now, we're ready to create our local environment!

Clone the repository, and navigate to the downloaded folder. This may take a minute or two to clone due to the included image data.
git clone https://github.com/udacity/CVND_Exercises.git
cd CVND_Exercises
Create (and activate) a new environment, named cv-nd with Python 3.6. If prompted to proceed with the install (Proceed [y]/n) type y.

# Linux or Mac:
conda create -n cv-nd python=3.6
source activate cv-nd
Windows:
conda create --name cv-nd python=3.6
activate cv-nd
At this point your command line should look something like: (cv-nd) <User>:CVND_Exercises <user>$. The (cv-nd) indicates that your environment has been activated, and you can proceed with further package installations.

Install PyTorch and torchvision; this should install the latest version of PyTorch.

Linux or Mac:
conda install pytorch torchvision -c pytorch 
Windows:
conda install pytorch-cpu -c pytorch
pip install torchvision
Install a few required pip packages, which are specified in the requirements text file (including OpenCV).

pip install -r requirements.txt
That's it!
Now all of the cv-nd libraries are available to you. Assuming you're environment is still activated, you can navigate to the Exercises repo and start looking at the notebooks:

cd
cd CVND_Exercises
jupyter notebook
To exit the environment when you have completed your work session, simply close the terminal window.

Notes on environment creation and deletion
Verify that the cv-nd environment was created in your environments:

conda info --envs
Cleanup downloaded libraries (remove tarballs, zip files, etc):

conda clean -tp
Uninstall the environment (if you want); you can remove it by name:

conda env remove -n cv-nd
