# Exercises for BSc Informatik - beverI HS 2023

This repository is used for the development and distribution of exercises for BSc Informatik - beverI HS 2023


## Working on the exercises

### Google Colab

Use Google Colab by clicking on the links below.


#### Exercise 01 - Machine Learning Recap

Click on the following badge to open the notebook in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/i4Ds/sgi-beveri-assignments-hs2023/blob/main/assignments/01_ml_recap/machine_learning_recap.ipynb)


### Jupyter-Hub

We provide you with the online platform JHub at 
[https://jhub.cs.technik.fhnw.ch](https://jhub.cs.technik.fhnw.ch). Use the image `sgi_bveri_hs2023`.

(Please be aware that on JHub only files that are in `/home/jovyan/work/persistent/` are safe from being deleted, when your server is being restarted, which can also occur due to maintenance reasons.)

If you want to use this option, proceed as follows:

#### 1. Fork this repository

Fork this repository to your own user space by pressing the fork button on the upper right.  

##### 2. Clone your fork to your workspace in JHub

In your fork on GitLab find the https-address (`MY_REPO_FORK_HTTPS_ADDRESS`), with which you can clone your Repo.  

Open a terminal window in JupyterLab, `cd` into `/home/jovyan/work/persistent` and clone your fork with:  

```
$ git clone MY_REPO_FORK_HTTPS_ADDRESS
```


#### 3. Fetching new assignments 

To fetch new assignments from the main repo do as follows:

```
# add original repo as remote upstream 
$ git remote add upstream https://gitlab.fhnw.ch/ml/courses/bveri/bveri-hs2023-exercises.git

# now whenever you want to merge the changes from the remote upstream repo,
# ie the one you forked from, you can do:
$ git pull upstream publish
```

.. and add some merge message in case you have to merge.


### Local Docker Setup

#### 1. Install Docker on your computer

Depending on your operating system you have to install docker in different ways.  

You'll find detailed instructions here: https://docs.docker.com/get-docker


#### 2. Pull the Docker image

You can pull the image with an API token that allows for reading the container registry:

```
# login to the FHNW GitLab docker registry first
$ docker login cr.gitlab.fhnw.ch -u <username> -p t6dzYJnu--rfaPSPYz-i

# now pull the image
$ docker pull cr.gitlab.fhnw.ch/ml/courses/bveri/bveri-hs2023-exercises:v20221208
```

#### 3. Fork this repository

Fork this repository to your own user space by pressing the fork button on the upper right.

#### 4. Clone your fork to your computer. 

For this you might wanna set up a ssh-key for your computer, see here:
https://docs.gitlab.com/ee/ssh/ . Otherwise you can also proceed with https.

In your fork on GitLab find the address (`MY_REPO_FORK_ADDRESS`) with which you can clone your Repo.

Clone into your ml directory (`MY_ML_DIR`) using:

```
$ git clone -b publish MY_REPO_FORK_HTTPS_ADDRESS
```


#### 5. Start a ml container on your machine

```
# Replace 'MY_ML_DIR' with your local code directory
$ docker run -d \
    -p 8877:8888 \
    --user root \
    -v MY_ML_DIR:/home/jovyan/work/ \
    --name=bveri_hs2023 \
    cr.gitlab.fhnw.ch/ml/courses/bveri/bveri-hs2023-exercises:v20221108 start.sh jupyter lab --LabApp.token=''
```

#### 6. Check that your container is running

```
$ docker ps -a
```

#### 7. Connect to your container through your browser

Enter `http://localhost:8877/lab` in your browser.


#### 8. Restart

If you later on need to restart your container you can just run

```
$ docker start bveri_hs2023
```


#### 9. Fetching new assignments 

To fetch new assignments from the main repo do as follows:

```
# add original repo as remote upstream 
$ git remote add upstream git@gitlab.fhnw.ch:ml/courses/bveri/bveri-hs2023-exercises.git

# now whenever you want to merge the changes from the remote upstream repo, ie
the one you forked from, you can do:
$ git pull upstream publish
```

.. and add some merge message in case you have to merge.

