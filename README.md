## TEAM DIRECTORY REPOSITORY

### [Author: Laura Uzcategui](www.github.com/laurauzcategui)

**************

This repository was done with the purpose of learning how to deploy Django applications on Heroku.

The Team Directory project was completed by following a codeschool tutorial, if you wish to followed by your own just [click here](https://www.codeschool.com/screencasts/build-a-team-directory-app-with-django)
*******

Otherwise feel free to clone the repository and follow the next steps if you want to try and deploy to heroku:

### 1.- Try out the application
```
# clone the repo
  $ git clone https://github.com/laurauzcategui/TeamDirectory.git
# from TeamDirectory folder create your own virtual - virtualenv [name_of_your_env]
  $ virtualenv envd
# Activate the virtual env
  $ source envd/bin/activate
# install the requirements you need for running the app
  $ pip install -r requirements.txt
# If you want to run the app locally
  $ python manage.py runserver
# Open a browser and go to your localhost  
  Type in Chrome : http://127.0.0.1:8000/
```
### 2.- Heroku deployment
```
# Install Heroku Command Line (depends on your OS)
  Heroku Command line: https://devcenter.heroku.com/articles/heroku-command-line
# Try to run the application locally first before deployment
  $ heroku local web
# If everything is up and running open in your browser
  Type in Chrome : http://localhost:5000/
# Login to heroku
  $ heroku login
# Create the application. It will display name of the application like:
https://git.heroku.com/[application_name].git
  $ heroku create
# Include as remote the repo for pushing to heroku
  $ heroku git:remote -a [application_name]
# Deploy to heroku
  $ git push heroku master
```
#### Issues I ran into:
  1. **No default language could be detected for this app.**
    * Solution: Configurations files like requirements.txt were misspelled
  2. **ImportError: No module named Directory.wsgi** Procfile should work only with :
    * Solution:
    ```
    web: gunicorn Directory.wsgi
    ```

### Feel free to collaborate :-)

#### Application deployed: [Young Beyond](https://young-beyond-42225.herokuapp.com/)
Note: It might not be available always ;-)
