Getting started
===============

**Dedub** is a DNN based identifier of similar ads by employing image and text modalities. It takes as input the image or text
or both information and identifies if two ads are duplicate/similar or not.

Technology stack
----------------
* Python 3.8.x: https://www.python.org/
* Tensoflow: https://www.tensorflow.org/
* Keras: https://keras.io/
* Transformers: https://huggingface.co/docs/transformers/index
* Pytest: https://docs.pytest.org/en/stable/
* Pytest-mock: https://github.com/pytest-dev/pytest-mock/
* Docker: https://www.docker.com/

Installation
-------------
The project requirements can be installed using Python's builtin package manager `pip` in a virtual environment
or by using `Docker`. Make sure that Python version `>= 3.8.x` is installed in your system (in case you will use docker you need to install
docker as well). With Python installed, change directory to a desired location and create a Python virtual environment,
with::

$ cd /path2/Dedub_venv
$ python -m venv Dedub_venv

Activate the virtual environment using::

$ source /path2_Dedub_venv/bin/activate
$ pip install -r requirements.txt

In the case of docker run the following to create the image::

$ sudo docker build -t dedub_network:1.0 .
