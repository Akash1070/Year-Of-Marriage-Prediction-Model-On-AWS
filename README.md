
# **End-To-End Deployment of Year Of Marriage Prediction Using AWS**
 The main agenda of this project is:

1. Perform extensive Exploratory Data Analysis(EDA) on the Marriage Dataset.

2. Build an appropriate Machine Learning Model that will help various Dar to predict their Year Of Marriage based on certain features

3. Deploy the Machine learning model via AWS that can be used to make live predictions of Year Of Marriage.
## Authors

- [@Akash Kumar Jha](https://github.com/Akash1070)


## Installation

To install the libraries used in this project. Follow the 
below steps:

```bash
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestRegressor
from sklearn.metrics import mean_absolute_error, r2_score
import pickle

```

## Deployment

To Deploy the libraries used in this project. Follow the 
below Codes:

Type the command ssh -i aws-key.pem ubuntu@(add your Private Private
IPv4 addresses) 

Type chmod 400 aws-key.pem to get rid of the error

Check to see if you have Python 3 installed: python3 -V
Let’s update all the existing packages: sudo apt-get update

Check if pip is installed, else install it. pip
If pip is not installed, download pip: curl -O https://bootstrap.pypa.io/get-pip.py
Update

Install pip: sudo python3 get-pip.py
Install Flask: sudo pip install flask

Install the following as well
sudo pip install flask_cors
 sudo apt-get install apache2
 sudo pip install sklearn
 sudo apt-get install libapache2-mod-wsgi-py3

Let’s do some configurations: sudo vi /etc/apache2/sites-enabled/000-default.conf
Copy and paste the following codes:
DocumentRoot /home/ubuntu/mlapp
WSGIDaemonProcess flaskapp threads=5 python-home=/usr/local/lib/python3.5/site-packages/ user=ubuntu
 WSGIScriptAlias / /home/ubuntu/mlapp/flaskapp.wsgi
<Directory /home/ubuntu/mlapp>
 WSGIProcessGroup flaskapp
 WSGIApplicationGroup %{GLOBAL}
 Require all granted
 </Directory>
 
 Now press escape(esc) followed by :wq! then press enter to exit
 
 Create file flaskapp.wsgi at mlapp directory
 The Web Server Gateway(wsgi) Interface is a simple calling convention for web servers to forward
requests to web applications
Steps:
irst create a directory: mkdir mlapp
cd to the directory: cd mlapp/
vi flaskapp.wsgi

import sys
import site
site.addsitedir(‘/home/ubuntu/.local/lib/python3.5/site-packages’)
sys.path.insert(0, ‘/home/ubuntu/mlapp’)
from app import app as application

Make sure you have saved your model and app.py file
Move your files to AWS
NB: do this from a new Terminal or Command Prompt 

cd to the deployment folder
Then type: scp -i (path to was key) -r app.py ubuntu@(add your public key here):/home/ubuntu/mlapp

Confirm to see if you have all files: ls
Restart the server: sudo apachectl restart
Check log incase you run into any error: cat /var/log/apache2/error.log

Use vi (File Name). to see the error and fix it.
restart the server again
Test your App by copying and pasting your public key (e.g. 157.36.87.192) into your browser

```
    
## Running Flask Api

To run tests, run the following command

```bash
  python app.py
```


## 🚀 About Me

Data Scientist Enthusiast | Petroleum Engineer Graduate | Solving Problems Using Data 


# Hi, I'm Akash! 👋


## 🔗 Links
[![github](https://img.shields.io/badge/github-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://github.com/Akash1070)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/akashkumar107/)
## Tech stack
![Logo](https://businesstoys.in/assets/programs/full-stack-data-science-professional-program/tools.png)


## Other Common Github Profile Sections
👩‍💻 I’m interested in Petroleum Engineering

🧠 I’m currently learning Data Scientist | Data Analytics | Business Analytics

👯‍♀️ I’m looking to collaborate on Ideas & Data




## 🛠 Skills
1. Data Scientist
2. Data Analyst
3. Business Analyst
4. Machine Learning 


## Future Plans 

⚡️ Looking forward to help drive innovations into your company as a Data Scientist

⚡️ Looking forward to offer more than I take and leave the place better than i found
