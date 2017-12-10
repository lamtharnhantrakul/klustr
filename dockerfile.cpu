
###########
#
#      DOCKER CONTAINER FOR MIR Project 2017
# MAINTAINED BY: Lamtharn (Hanoi) Hantrakul -- hanoi@smartear.io | hanoi7@gmail.com | lhantrakul3@gatech.edu
# The purpose of this container is to provide a stable base image for our projected called "Klustr" by
# Lamtharn (Hanoi) Hantrakul and Avneesh Sarwate
#
# Please add new pip/apt installs in this block. Don't forget a "&& \" at the end
# of all non-final lines. Thanks!
#
###########

### Pull official Anaconda Python Distribution 4.4.0 (which has python 2.7)
FROM continuumio/anaconda:4.4.0

### Install custom libraries

# Progress bar
RUN pip install tqdm

# Install Matplotlib
RUN conda install matplotlib

# Install Shapely for metrics related to shapes
RUN pip install shapely

# Install librosa
RUN pip install librosa

# Instructions for installing UMAP
RUN conda install numpy scipy
RUN conda install scikit-learn
RUN conda install numba
RUN pip install umap-learn

# Set working directory to /klustr
WORKDIR /klustr

# Copy all current directory contents into the container at /klustr
ADD . /klustr
