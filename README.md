Example Uber app for developers
==============================

This is a simple Python/Flask application intended to provide a working example of Uber's external API. The goal of these endpoints is to be simple, well-documented and to provide a base for developers to develop other applications off of.

This application uses vagrant and packer to create automated development and production environments that are provisioned with Chef cookbooks. 


How To Use This
---------------

1. Clone the following repository: https://github.com/Neveen-E/Python-Sample-Application
2. Navigate to the project folder and type in the following commands to create and configure a virtual machine:

 ``` 
vagrant up 
vagrant ssh
```
3. When the vagrant machine is running, type in the following `pip install -r requirements.txt` to install the app's dependencies.
4. Type `python app.py` to run the application.
5. Use the following link to open the application on any browser `http://development.project`
