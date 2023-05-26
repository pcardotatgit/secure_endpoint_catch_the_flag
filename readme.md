# Cisco Secure Threat Hunting Challenge

This challenge is a Cisco Secure Endpoint ( AMP for Endpoint ) Threat Hunting challenge.


Here is an observable : **01468b1d3e089985a4ed255b6594d24863cfd94a647329c631e4f4e52759f8a9** 

Question 1 : How many Endpoints are targeted by this sha256 in your organization ?

Question 2 : What are the targeted Endpoints hostnames ?

## Your Mission

Write a python script which gives you the answer what ever the AMP observable is.

The **solution** Folder contains an example of such solution.   But you have to troubleshoot the script

Go to : 

https://api-docs.amp.cisco.com/

And figure out what is the AMP API URL endpoint which can help you to get the final answer.

The API endpoint into which you can pass a sha256 as argument, and which gives you into it's JSON result, hostnames of infected machines.

# Install your CTF lab environment

You don't need any Cisco Secure Endpoint Account for this challenge, we provide you with and AMP backend simulator located into the **amp_simulator** folder

Create a working directory into you laptop, then go into it.

You can download the code from this page in the .zip format by clicking on the green **code** button on the top right, and then select **Download Zip**.

Next step is to unzip the content of the zip file into your working directory. You will be ready to go.

Or another solution is, if you have a git client into your laptop to use it. 
For this open a CMD console and go to this directory.

Clone the challenge code from github :

	git clone https://github.com/pcardotatgit/secure_endpoint_catch_the_flag.git

## AMP backend Simulator Installation

Change directory to the directory where is located the AMP backend Simulator **./amp_simulator**.

	cd c:.../your_working_directory/secure_endpoint_catch_the_flag/amp_simulator

### Install and start a Python virtual environment

For Linux/Mac 

	python3 -m venv venv
	source bin activate

For Windows 
	
We assume that you already have installed git-bash.  If so open a git-bash console and type the 2 following commands :

	python -m venv venv 
	venv\Scripts\activate
	
### install needed modules
	
	python -m pip install --upgrade pip
	pip install -r requirements.txt

### Run the simulator

	python amp_sim.py
	
You should see the server start. It listens on https 4000.	
	
	(venv) C:\Users\pcardot\Documents\tests\01_amp_challenge\amp_simulator>python amp_sim.py
	 * Serving Flask app "amp_sim" (lazy loading)
	 * Environment: production
	   WARNING: This is a development server. Do not use it in a production deployment.
	   Use a production WSGI server instead.
	 * Debug mode: on
	 * Restarting with stat
	 * Debugger is active!
	 * Debugger PIN: 162-768-494
	 * Running on https://0.0.0.0:4000/ (Press CTRL+C to quit)

On your windows laptop, allow the amp simulator to listen on port 4000 when the Firewall authorization windows will popup.

# You are ready to go to the challenge

A python script named **student_code.py** is available for you into the **solution** folder.

Open a second CMD console and Go to the **solution** folder.

For this code you must create a python virtual environment as well, and you must activate it.

For windows :

	python -m venv venv 
	venv\Scripts\activate

For this script you need to install the **requests** and the **crayons** modules

	pip install requests
	pip install crayons

- Then Run the **student_code.py** file and follow the instructions.

The principle of this challenge is to troubleshoot the **student_code.py** script.  For this You can just run it and it will automatically break every time you have a troubleshooting action to perform.

example :

	TODO :
	124
	First : assign the correct value to the variable : sha
	Change the value of i_got_it to 1 in order to move forward

**124** is the line number in the code where the script broke.  Go to this line and look for the instructions around, fix the code. 

Set the **i_got_it** variable to 1 **( i_got_it=1 )**.

And then run it again until the next break.

Step by step you will find the answers to all questions until the final one !  who is infected by this sha256 into your organization? ?

## Quizz

You have 30 mins to find the answers for the following questions that will be asked to you by the script :

1 - What is the value of the AMP_API_KEY ?
2 - What is the value of the sha256 we want to investigate ?
3 - Which python function to call and how to call it ?
4 - What is the correct Secure Endpoint API to use for get infected machine hostnames ?
5 - How many Endpoint are targeted by this threat ?
6 - What are the infected hostnames ?

## Bonus Challenge

Send the answers into your Webex Team Room

