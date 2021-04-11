# flask-login-tutorial
Code from [Anthony Herbert's Digitalocean article "How To Add Authentication to Your App with Flask-Login"](https://www.digitalocean.com/community/tutorials/how-to-add-authentication-to-your-app-with-flask-login) with minor changes as follows:

* Tabs for indentation instead of spaces. I know PEP-8 styleguide prefers spaces, however I find this a mind-numbingly bad default and will gleefully thumb my nose at it whenever I get the chance; tabs are more flexible.
* Step 6 changes that will be noted below
* remove extraneous spaces around <a> tags in the template documents
* reorganization of the navbar links in step 10 to prevent the need for multiple is_authenticated ifs


## Step 6 Changes

included in the base of the project from Step 6 onwards is an extra file, [dbcreate.py](https://github.com/adhesivecheese/flask-login-tutorial/blob/main/dbcreate.py), that is a 2 line script that should be run to set up the database, instead of running commands from a python shell. This is included for convenience, in order to have all the code needed to run this project in this repo, as well as to fix an error in the instructions: models must be imported on line 1, and this is missing from the tutorial. This file should be run by issuing

    python3 createdb.py
    
in the directory the `flask-login-tutorial` directory.

## Should the tutorial disappear/you just want to run the code
1. Checkout the master repository
2. install requirements with `pip install -r requirements.txt`
3. run createdb as indicated earlier
4. set enviornment variables as follows: `export FLASK_APP=project` and `export FLASK_DEBUG=1`
5. run the dev server with `flask run`
