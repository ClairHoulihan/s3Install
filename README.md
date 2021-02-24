# s3Install
A helpful Doc for getting s3 working on your machine

## Installing s3cmd

These points are made with Windows running WSL Ubuntu in mind, if you are using mac or another os, there will be some different commands then the ones shown.

1. The first thing you will want to do is install pip. Pip is an installer built with Python to install python libraries. Very similar to apt.
  To install, go ahead and run this command:`sudo apt update` the run: `sudo apt install python3-pip`
  
2. Make sure to install python as well if you do not already have it, you can do so with this command `sudo apt install python`

3. You will also want to download the s3cmd zip file from here: https://s3tools.org/s3cmd (just download the latest version from source forge)

4. Unzip the file in your wsl (I used unzip for this, you can download the command using `sudo apt install unzip`)

5. Go into the newly created file and run `sudo pip3 install s3cmd` to get all of the dependencies, then run `sudo python3 setup.py install`

6. You will need the python-dateutil which you can install using `sudo apt-get install python-dateutil`

7. You will want to run the configuration for s3cmd, but before that, you will need to get an access key and a secret key. To get them, log into your aws account and go to your iam security credentials, you can access it here when you log in: https://console.aws.amazon.com/iam/home?#/security_credentials

8. Click on access keys, and create a new access key, make sure to save these keys, you will use them next.

9. Run ./s3cmd --configure and give the application the access key and secret key where it is prompted. Everything else you should be able to leave blank (although for encryption password, I would put in something you can remember, but different from other passwords that you have).

10. Go ahead and test the connection at the end, if it works, you should be able to continue using s3cmd without issue, if there are problems that occur during any step, let me know, and I will attempt to solve it (and perhaps add it to this README so that others can see it if they have the same problem).
  
