# Lab 2 - Using an existing image to create a project
In this lab you will create and run a project from an existing container image.

    Deploying existing images to OpenShift: video (7:09 mins)

## Overview

This is a quick lab that demonstrates how to deploy a public image from Docker Hub on OpenShift. As example image the 'authors' microservice from this workshop is used.

Note: Not all images from Docker Hub can be installed. For example OpenShift doesn't allow to deploy images which run under 'root'. See the OpenShift documentation for details.
### Step 1

Open the OpenShift Console from the IBM Cloud OpenShift dashboard.
### Step 2

Create a new project 'workshop'.
### Step 3

Open the new project.
### Step 4

Click 'Add to Project', followed by 'Deploy Image' in the pop up menu and then 'Deploy Image' in the dialog.
### Step 5

Enter 'nheidloff/authors:v1' as the image name, click the search icon and then the 'Deploy' button.
### Step 6

Navigate back to the overview page.
### Step 7

Click 'Create Route'.
### Step 8

Click the 'Create' button (not shown in the screenshot).
### Step 9

Copy the URL and append '/openapi/ui'.

add /openapi/ui to the end of the URL
### Step 10

Open the Open API user interface to try the REST API.
### Stretch Goal: Use your own Image

You can deploy your image from the next Lab 3.

If you want you can make changes to the Java code and/or image and push these changes to your own Docker Hub account. In order to do this, you need a Docker Hub account and invoke these commands:

$ cd ${ROOT_FOLDER}/2-deploying-to-openshift
$ DOCKER_ACCOUNT=<your-docker-account>
$ docker login
$ docker build -t $DOCKER_ACCOUNT/authors:v1 .
$ docker push $DOCKER_ACCOUNT/authors:v1

## Success!

Congratulations! You finished Lab 2, and deployed an image from a public registry aviable from Docker Hub.

You might follow more labs on OpenShift with pre-provisioned clusters here: https://github.com/IBM/openshift-on-ibm-cloud-workshops/blob/master/2-deploying-to-openshift/documentation/6-github.md

You can go to Lab 3 or start to use MiniShift on your platform as it is defined in the Next Steps.
