Dedub - Ads Similarity Network
========

All the functionalities of these project are exposed to the three python run_* scripts which are located at the top
level of the project.

Dedub Functionalities
^^^^^^^^^^^^^^^^^^^^^

* This command will download the raw files based on the env var "DATA_URL' and preprocess them based on the configuration file::

    $ python run_make_dataset.py --config src/config/config.py

In order to be able to retrieve the data you need to create a **.env** file at the root directory and export inside of it a `DATA_URL` environmental variable
with the link to the raw data.

* This command will train a DNN by using text or image or both modalities depending on the configuration::

    $ python run_make_dataset.py --config src/config/config.py`

*  This command will run a prediction by choosing which network to use based on the input of arguments.
   If only titles are provided will use a DNN for text modalities, if only images are provided will use a DNN for
   image modalities and if both are provided will uses the model for all the modalities::

    $ python run_inference.py --config src/config/config.py

* Run everything with docker (See installation section to see how to build the image)::

    $ sudo docker run --name dedub_image dedub_network:1.0 python run_train.py --config src/config/config.yaml
