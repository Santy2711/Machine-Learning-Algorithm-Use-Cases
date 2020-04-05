# Machine-Learning-Algorithm-Use-Cases(Linear Regression till Deployment )

Deployment Link : https://mllearningdeployment.appspot.com/


Cloud Deployment (Google Cloud Platform)

Once the training is completed, we need to expose the trained model as an API for the user to consume it. For prediction, the saved model is loaded first and then the predictions are made using it. If the web app works fine, the same app is deployed to the cloud platform.

![Image-1](https://user-images.githubusercontent.com/61689146/78499716-e6376580-7784-11ea-8d1b-295c6960da5b.png)



Pre-requisites:

Basic knowledge of flask framework.
Any Python IDE installed(we are using PyCharm).
A Google Cloud Platform account.
Basic understanding of HTML.
Flask App

As we’ll expose the created model as a web API to be consumed by the client/client APIs, we’d do it using the flask framework. The flow of our flask app will be:

![image-2](https://user-images.githubusercontent.com/61689146/78499752-0e26c900-7785-11ea-93b7-3d70dc18d0ec.png)

Create the project structure, as shown below:

![image-3](https://user-images.githubusercontent.com/61689146/78499758-1848c780-7785-11ea-9bc0-2bcabc747321.png)


Deployment to G-cloud:

Go to https://cloud.google.com/ and create an account if already haven’t created one. Then go to the console of your account.
Go to IAM and admin(highlighted) and click manage resources.

![image-4](https://user-images.githubusercontent.com/61689146/78499766-1f6fd580-7785-11ea-8ec2-98b19a87e006.png)

. Click CREATE PROJECT to create a new project for deployment.

. Once the project gets created, select App Engine and select Dashboard.

![image-5](https://user-images.githubusercontent.com/61689146/78499785-46c6a280-7785-11ea-98eb-48930be65162.png)


. Go to https://dl.google.com/dl/cloudsdk/channels/rapid/GoogleCloudSDKInstaller.exe to download the google cloud SDK to your machine.

. Click Start Tutorial on the screen and select Python app and click start.

![image-6](https://user-images.githubusercontent.com/61689146/78499788-4a5a2980-7785-11ea-8f27-e2eabfd102a6.png)

. Check whether the correct project name is displayed and then click next.

![image-7](https://user-images.githubusercontent.com/61689146/78499789-4b8b5680-7785-11ea-9ec0-b014c58a0f26.png)

.Create a file ‘app.yaml’ and put ‘runtime: python37’ in that file.

.Create a ‘requirements.txt’ file by opening the command prompt/anaconda prompt, navigate to the project folder and enter the   command ‘pip freeze > requirements.txt’. It is recommended to use separate environments for different projects.

.Your python application file should be called ‘main.py’. It is a GCP specific requirement.

.Open command prompt window, navigate to the project folder and enter the command gcloud init to initialise the gcloud context.
.It asks you to select from the list of available projects.



![image-8](https://user-images.githubusercontent.com/61689146/78499790-4c23ed00-7785-11ea-9009-07db51ece608.png)

.Once the project name is selected, enter the command gcloud app deploy app.yaml --project

.After executing the above command, GCP will ask you to enter the region for your application. Choose the appropriate one.

![image-9](https://user-images.githubusercontent.com/61689146/78499792-4c23ed00-7785-11ea-8fdf-07caf45dbb03.png)

.GCP will ask for the services to be deployed. Enter ‘y’ to deploy the services.

.And then it will give you the link for your app,and the deployed app looks like:

![image-10](https://user-images.githubusercontent.com/61689146/78499816-71b0f680-7785-11ea-9311-b778e2ac216a.png)


![image-11](https://user-images.githubusercontent.com/61689146/78499819-770e4100-7785-11ea-8784-2494274cc0b9.png)

