# Introduction

This Flask project is intended to serve as an advertisment for BU Jalwa.

The project is intended to be submitted as part of remediation project for WR152 at Boston University. The aspects of the website such as the layout and motivations/demotivations for joining the team were concluded using the results from the research paper "Understand the Motivations and Demotivations for Collegiate Competitive Dance" by Anurag Mathews (anuragm1@bu.edu).

Thanks for checking it out!

# Local Deployment
## Create a virtual environment
```
mkdir myproject
cd myproject
py -3 -m venv .venv
```

## Activate the environment
```
.venv\Scripts\activate
```

## Install Flask
When inside the environment, install Flask.

```
$ pip install Flask
```

## Start Server
Start the server with:
```
flask run
```
or
```
flask run --debug
```
for easy debugging.

# Online Deployment
## PythonAnywhere

### Initial Deployment
Begin by logging into your PythonAnywhere account and opening a bash terminal.

Generate an SSH Key with:
```
ssh-keygen
```
When prompted with default ssh key location hit enter.
Feel free to hit enter twice more to skip through the passphrase.

Print the ssh key to terminal with:
```
cat .ssh/id_rsa.pub
```
Then, copy the entire ssh key which should look something like (ellipses covering extended ssh):
```
ssh-rsa A...y0= BUJalwa@green-liveconsole4
```
Next, open github.
Go to profile picture in top right > settings > SSH and GPG Keys and create add the new SSH Key.
After clicking new key, paste the key into the text box, select Authentication Key, and give it a title.
Then click Add SSH Key.

Congrats you have connected PythonAnywhere to your Github Account!

Now to clone your repository, go to your repository on github. Click Code > SSH and copy the url.

Go back to your terminal and enter:
```
git clone git@github.com:Skyhawk123456789/BUJalwa.git
```
When prompted to connect, type yes.

Go back to the main PythonAnywhere screen and go to the Web tab and click Add a new web app.
Click Next, select Flask from the options, select your version of Python.
Replace the path with the path to your main App.py. Hit next.

Finally, you must manually replace your App.py with the one from Github and PythonAnywhere writes over it.

### For future updates.
To update your project for new changes to github run the following.
Open your bash console and enter:
```
cd /home/BUJalwa/BUJalwa
git pull
```
