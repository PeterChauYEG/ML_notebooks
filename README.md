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
2. Run the container:
```
docker run -it -p 8888:8888 -p 6006:6006 -v /$(pwd)/ML_notebooks:/notebooks -e "TENSORFLOW_VERSION=1.3.0" --name jupyter pkmital/cadl:latest /bin/bash
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

## OpenAI Universe
- install openai Universe
```
git clone https://github.com/openai/universe.git
cd universe
pip install -e .
pip install Twisted==16.0.0
```

- OSX needs some other packages
```
pip install numpy incremental
sudo brew install golang libjpeg-turbo
```

- `docker build -t universe .`
- test that it works: `docker run --privileged --rm -e DOCKER_NET_HOST=172.17.0.1 -v /var/run/docker.sock:/var/run/docker.sock universe pytest`
`
- run a dev container`docker run --privileged --rm -it -e DOCKER_NET_HOST=172.17.0.1 -v /var/run/docker.sock:/var/run/docker.sock -v /${pwd}:/usr/local/universe universe python`

## Notebook practice implementation source
1. [MNIST Classifier](https://github.com/amygdala/tensorflow-workshop/blob/master/workshop_sections/mnist_series/mnist_simple.py)
