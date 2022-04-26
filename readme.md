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

And figure out what is the AMP API URL endpoint which can help you to get the answer.

# Install your CTF lab environment

You don't need any Cisco Secure Endpoint Account for this challenge, we provide you with and AMP backend simulator located into the **amp_simulator** folder

Create a working directory into you laptop, open a CMD console and go to this directory.

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

A solution python script template is available for you.

Go to the **solution** folder.

- Run the **student_code.py** file and follow the instructions.

The principle of this challenge is to troubleshoot the **student_code.py** script.  You can just run it and it will automatically break every time you have a troubleshooting action to perform.

example :

	TODO :
	124
	First : assign the correct value to the variable : sha
	Change the value of i_got_it to 1 in order to move forward

**124** is the line number in the code where the script broke.  Go to this line and fix the code. 

Set the **i_got_it** variable to 1 **( i_got_it=1 )**.

And then run it again until the next break.

Troubleshooting every voluntary bugs until you get the answers to the questions.

## Bonus Challenge

Send the answers into your Webex Team Room

