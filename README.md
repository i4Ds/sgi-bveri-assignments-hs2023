# Exercises for BSc Informatik - bveri HS 2023

This repository is used for the development and distribution of exercises for BSc Informatik - bveri HS 2023


There are several ways to work on the assignments:

- Google Colab (easiest)
- local - pip install (not tested)
- Jupyter-Hub (easy but no GPU)
- local - Docker


## Google Colab

Use Google Colab by clicking on the links below.


### Exercise 01 - Machine Learning Recap

Click on the following badge to open the notebook in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/i4Ds/sgi-bveri-assignments-hs2023/blob/main/assignments/01_ml_recap/machine_learning_recap.ipynb)


### Exercise 02 - PyTorch & Machine Learning

Click on the following badge to open the notebook in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/i4Ds/sgi-bveri-assignments-hs2023/blob/main/assignments/02_pytorch/pytorch.ipynb)


### Exercise 03 - Neuronale Netzwerke

Click on the following badge to open the notebook in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/i4Ds/sgi-bveri-assignments-hs2023/blob/main/assignments/03_neural_networks/neural_networks.ipynb)


### Exercise 04 - Convolutional Neural Networks

Click on the following badge to open the notebook in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/i4Ds/sgi-bveri-assignments-hs2023/blob/main/assignments/04_cnns/cnns.ipynb)


### Exercise 05 - Image Classification

Click on the following badge to open the notebook in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/i4Ds/sgi-bveri-assignments-hs2023/blob/main/assignments/05_classification/classification.ipynb)


### Exercise 06 - Object Detection

Click on the following badge to open the notebook in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/i4Ds/sgi-bveri-assignments-hs2023/blob/main/assignments/06_object_detection/object_detection.ipynb)


### Exercise 07 - Segmentation

Click on the following badge to open the notebook in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/i4Ds/sgi-bveri-assignments-hs2023/blob/main/assignments/07_segmentation/segmentation.ipynb)




## Local - pip (not tested)

```
pip install -r requirements.txt
```


## Jupyter-Hub (CPU only)

We provide you with the online platform JHub at 
[https://jhub2.cs.technik.fhnw.ch](https://jhub2.cs.technik.fhnw.ch). Use the image `sgi_bveri_hs2023`.

(Please be aware that on JHub only files that are in `/home/jovyan/work/persistent/` are safe from being deleted, when your server is being restarted, which can also occur due to maintenance reasons.)

If you want to use this option, proceed as follows:

### 1. Fork this repository

Fork this repository to your own user space by pressing the fork button on the upper right.  

#### 2. Clone your fork to your workspace in JHub

In your fork on GitLab find the https-address (`MY_REPO_FORK_HTTPS_ADDRESS`), with which you can clone your Repo.  

Open a terminal window in JupyterLab, `cd` into `/home/jovyan/work/persistent` and clone your fork with:  

```
$ git clone MY_REPO_FORK_HTTPS_ADDRESS
```

**Tipp**: You can use an access API token to avoid having to type your username and password, as well as confirming logins with 2FA.

To use an API token, on GitLab in your fork of the repository:

"Settings->Access Tokens"

1. Enter a name for your access token
2. Select an expiration date well after this course ends
3. Select the maintainer role
4. Select "api" under scopes
5. Create token and save it  (`MY_ACCESS_TOKEN`)
6. Find the address of your repo without the https prefix (`MY_REPO_FORK_ADDRESS_NO_HTTPS`)

Then you can clone the repository with the following command:

```
git clone https://api:MY_ACCESS_TOKEN@MY_REPO_FORK_ADDRESS_NO_HTTPS
```

example:

```
git clone https://api:thisisnotaRealtoken@gitlab.fhnw.ch/marco.willi/bveri-exercises-hs2023
```

You might also have to set your user name and email once (replace accordingly):

```
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```


### 3. Fetching new assignments 

To fetch new assignments from the main repo do as follows:

```
# add original repo as remote upstream 
$ git remote add upstream https://gitlab.fhnw.ch/ml/courses/bveri/hs2023/bveri-exercises-hs2023

# now whenever you want to merge the changes from the remote upstream repo,
# ie the one you forked from, you can do:
$ git pull upstream main
```

.. and add some merge message in case you have to merge.


## Local - Docker

### 1. Install Docker on your computer

Depending on your operating system you have to install docker in different ways.  

You'll find detailed instructions here: https://docs.docker.com/get-docker


### 2. Pull the Docker image

You can pull the image with an API token that allows for reading the container registry:

```
# login to the FHNW GitLab docker registry first
$ docker login cr.gitlab.fhnw.ch -u <username> -p -tr6TtDDnCuoaJWtvbYz

# now pull the image
$ docker pull cr.gitlab.fhnw.ch/ml/courses/bveri/hs2023/bveri-exercises-hs2023:latest
```

### 3. Fork this repository

Fork this repository to your own user space by pressing the fork button on the upper right.

### 4. Clone your fork to your computer. 

For this you might wanna set up a ssh-key for your computer, see here:
https://docs.gitlab.com/ee/ssh/ . Otherwise you can also proceed with https.

In your fork on GitLab find the address (`MY_REPO_FORK_ADDRESS`) with which you can clone your Repo.

Clone into your ml directory (`MY_ML_DIR`) using:

```
$ git clone MY_REPO_FORK_HTTPS_ADDRESS
```

**Tipp**: You can use an access API token to avoid having to type your username and password, as well as confirming logins with 2FA.

To use an API token, on GitLab in your fork of the repository:

"Settings->Access Tokens"

1. Enter a name for your access token
2. Select an expiration date well after this course ends
3. Select the maintainer role
4. Select "api" under scopes
5. Create token and save it  (`MY_ACCESS_TOKEN`)
6. Find the address of your repo without the https prefix (`MY_REPO_FORK_ADDRESS_NO_HTTPS`)

Then you can clone the repository with the following command:

```
git clone https://api:MY_ACCESS_TOKEN@MY_REPO_FORK_ADDRESS_NO_HTTPS
```

example:

```
git clone https://api:thisisnotaRealtoken@gitlab.fhnw.ch/marco.willi/bveri-exercises-hs2023
```


### 5. Start a ml container on your machine

```
# Replace 'MY_ML_DIR' with your local code directory
$ docker run -d \
    -p 8877:8888 \
    --user root \
    -v MY_ML_DIR:/home/jovyan/work/ \
    --name=bveri_hs2023 \
    cr.gitlab.fhnw.ch/ml/courses/bveri/hs2023/bveri-exercises-hs2023:latest start.sh jupyter lab --LabApp.token=''
```

### 6. Check that your container is running

```
$ docker ps -a
```

### 7. Connect to your container through your browser

Enter `http://localhost:8877/lab` in your browser.


### 8. Restart

If you later on need to restart your container you can just run

```
$ docker start bveri_hs2023
```


### 9. Fetching new assignments 

To fetch new assignments from the main repo do as follows:

```
# add original repo as remote upstream 
$ git remote add upstream git@gitlab.fhnw.ch:ml/courses/bveri/hs2023/bveri-exercises-hs2023.git

# now whenever you want to merge the changes from the remote upstream repo, ie
the one you forked from, you can do:
$ git pull upstream
```

.. and add some merge message in case you have to merge.

