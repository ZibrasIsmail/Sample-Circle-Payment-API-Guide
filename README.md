# Sample-Circle-Payment-API-Guide

A simple circle payment API to use circle payment API to setting up the wallet and top up the wallet for development work

# Steps to access the Circle API and set up the wallet and top up the wallet 
Step 1: Set up a Circle API account
Step 2: Set up Postman
Step 3: Making Card Top Up in the Sandbox Environment to the Circle wallet
Step 4: Check the wallet by Making an API Call using Postman

# What is Circle Payment API?
Circle Payment API is a developer platform that allows businesses to accept and process payments securely and efficiently. It is designed to be easy to use and to provide developers with a flexible set of tools to integrate payments into their applications and websites.

# What can it do?
Circle Payment API provides a variety of payment processing capabilities, including the ability to:

Accept credit and debit card payments
Process bank transfers
Accept payments from digital wallets
Store and manage payment information securely
Issue refunds and cancellations

# How does it work?
To use Circle Payment API, developers need to create an account with Circle and obtain API credentials, including an API key and secret. The API supports both REST and WebSocket protocols and allows developers to send and receive data in JSON format.

Step 1: Set up a Circle API account

Before you can use the Circle Payments API, you need to create a Circle API account. You can sign up for an account at [https://developers.circle.com/signup](https://app-sandbox.circle.com/signup/sandbox). Once you have an account, you will be able to access the API key and secret that you need to make API requests.

* on the Sign up page fill all the details and once you click the sign up then it will tell to set up the authenticator to login everytime. you can prefer android or iphone device then use the google authendicator to scan the QR and do the necessary steps to do the authentication

# the home page of the circle account look like this

![Homepage](https://user-images.githubusercontent.com/59764125/219003356-56ae33c3-64a8-468f-978e-0ab1773d649d.png)


Step 2: Set up Postman

If you haven't already, download and install Postman from https://www.postman.com/downloads/. Postman is a popular tool for making API requests and testing APIs.

* download the postman and ready to test top up transaction details using the Payment API at the end

Step 3: Making Card Top Up in the Sandbox Environment to the Circle wallet

To understand how card payment works with Circle Payment API, we will be using a sample web application provided by Circle. We first need to install several programs. 

The first program to install is Git. Git is a distributed version control system that is used to track changes in files. For this quest, we will be using Git to clone the repository of the web application to show how card payment works in the sandbox environment. Cloning in Git is basically downloading a local copy of that online repository onto your file system. To check if you have installed Git, you can run the following command in your terminal or command line.
`git -v`

The next program to install is Node.js which is needed to run the web application. You can check if you have already installed Node.js using the command.
# node -v

The next program you will need to install is Yarn. Yarn is a Node.js package manager which is used to download the required libraries to run web applications. These libraries are not pre-installed in the repository because it would make the repository's overall file size too large and affect the download times. Usually, these libraries can range from a few megabytes (MB) to several gigabytes (GB). Therefore, the standard practice to store your Node.js application on the repository is to exclude any external libraries and then require the users who cloned the repository to download the required library using a Node.js package manager. This way, you can keep your repository small and compact. 
You can check if you have Yarn installed using the following command.
# yarn --version

If it does not return a version number, then you can run the following command to install Yarn. The next command uses npm (Node Package Manager), which is another Node.js package manager automatically installed when installing Node.js. The reason why we are using Yarn is because this web application is set up to use Yarn.
# npm install --global yarn

1. Now that you have installed the required programs, we will clone the needed repository to a local destination. To do so, open your terminal and navigate to your desired file location. In your desired file location in your terminal or command line, run the following command.
# git clone https://github.com/circlefin/payments-sample-app.git

2. Once you have cloned the repository, change your directory to the directory you just cloned with the following command.
# cd payments-sample-app

3. Next, you will need to create a .env file. This will contain the environment variables that will be loaded into the web application upon start up. An environment variable is a dynamic-named value that changes based on the environment chosen. We need the environment variable to hold the URL of the sandbox payment API as the web application will read the URL from here. By having multiple instances of these .env files, you can switch the URL according to where you want it to point to. But in our case, we will only need to create one .env file. The following command is used to create the .env file and configure the base URL for API calls.
# echo BASE_URL=https://api-sandbox.circle.com > .env

4. After creating the .env file, install the required libraries using the following command.
# yarn install

5. Once the libraries have been installed, you can start the web application server with this next command.
# yarn dev

Note: Once the web application server is running, you can access the web application via http://localhost:3011/ on your browser.
