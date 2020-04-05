# Machine-Learning-Algorithm-Use-Cases(Linear Regression till Deployment )

Deployment Link : https://mllearningdeployment.appspot.com/


Cloud Deployment (Google Cloud Platform)

Once the training is completed, we need to expose the trained model as an API for the user to consume it. For prediction, the saved model is loaded first and then the predictions are made using it. If the web app works fine, the same app is deployed to the cloud platform.

image -1


Pre-requisites:

Basic knowledge of flask framework.
Any Python IDE installed(we are using PyCharm).
A Google Cloud Platform account.
Basic understanding of HTML.
Flask App

As we’ll expose the created model as a web API to be consumed by the client/client APIs, we’d do it using the flask framework. The flow of our flask app will be:

image-2

Create the project structure, as shown below:

Image-3


Deployment to G-cloud:

Go to https://cloud.google.com/ and create an account if already haven’t created one. Then go to the console of your account.
Go to IAM and admin(highlighted) and click manage resources.

Image-4

. Click CREATE PROJECT to create a new project for deployment.

. Once the project gets created, select App Engine and select Dashboard.

image-5


. Go to https://dl.google.com/dl/cloudsdk/channels/rapid/GoogleCloudSDKInstaller.exe to download the google cloud SDK to your machine.

. Click Start Tutorial on the screen and select Python app and click start.

Image-6

. Check whether the correct project name is displayed and then click next.

Image-7

.Create a file ‘app.yaml’ and put ‘runtime: python37’ in that file.

.Create a ‘requirements.txt’ file by opening the command prompt/anaconda prompt, navigate to the project folder and enter the   command ‘pip freeze > requirements.txt’. It is recommended to use separate environments for different projects.

.Your python application file should be called ‘main.py’. It is a GCP specific requirement.

.Open command prompt window, navigate to the project folder and enter the command gcloud init to initialise the gcloud context.


Image-7

.Once the project name is selected, enter the command gcloud app deploy app.yaml --project

.After executing the above command, GCP will ask you to enter the region for your application. Choose the appropriate one.

Image-8

.GCP will ask for the services to be deployed. Enter ‘y’ to deploy the services.

.And then it will give you the link for your app,and the deployed app looks like:

Image-9
Image-10
.It asks you to select from the list of available projects.

