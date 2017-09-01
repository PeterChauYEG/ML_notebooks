# Machine Learning Notebooks
What is this? 

This is my set of practice implementations of common machine learning algorithms. 
It's me working through a bunch of great pet machine learning algoritms.

You can view them in the github repository as it can display Jupyter notebooks.

## Installation
The [notebooks](https://jupyter.org/) will need a number of dependancies including:
```
python 3
numpy
matplotlib
jupyter
tensorflow
```

I just use a [docker](https://www.docker.com/ container as my data science environment.

Here's how I set it up:
0. Clone this repository: `git clone https://github.com/PeterChauYEG/ML_notebooks.git`
1. Install docker
2. Get an appropraiate image. I use the [Creative Applications of Deep Learning w/ Tensorflow](https://github.com/pkmital/CADL) image
`git clone https://github.com/pkmital/CADL.git`
3. Change directories and build the Dockerfile:  
```
cd CADL
docker build -t jupyter .
```
4. Change directories and run the container:
```
cd ../..
docker run -it -p 8888:8888 -p 6006:6006 -v /$(pwd)/ML_notebooks --name jupyter jupyter /bin/bash
```
5. You should now be in the docker container's shell. You should see this repository's file's that were cloned to your device: `ls`
6. Start your jupyter notebook: `jupyter notebook`
7. Copy the link and go to it in a browser: `http://localhost:8888/`
8. Open a notebook and run the cells
9. To start the docker container again:
```
cd ~
docker start -i jupyter /bin/bash
```

## Notebook practice implementation source
1. [MNIST Classifier](https://github.com/amygdala/tensorflow-workshop/blob/master/workshop_sections/mnist_series/mnist_simple.py)













```
```
