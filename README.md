#MyApp Git Tutorial

To install git go to:
    Windows            https://git-scm.com/download/win
    Linux/Unix/MacOS   https://git-scm.com/download/

Install it with default parameters and Launch Git Bash in Wizard

(in the following symbol # after typed commands means answer under command line)

Type 
    git --version
    #git version 2.11.1.windows.1

Create folder in your Desktop 
    Type
        mkdir myApp

Go to this folder or open GitBash by clicing Mouse Right Click -> open GitBash here

Create a couple files:
    touch index.html
    touch app.js

Open your Code Editor and change index.html:
    <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <meta http-equiv="X-UA-Compatible" content="ie=edge">
            <title>Document</title>
        </head>
        <body>
            This is my app
        </body>
        </html>

Save file and initialize the folder as git repository:
    Type:
        git init

Add yuor user name and email:
 (--global means that this username and email will be used evrywere on this system. If you want to use different names or emails to folder symply do not type --global)
        git config --global user.name 'John Joseph'
        git config user.email 'email@example.com'

Lets add index.html after changing file in the previous step:
    Type:
        git add index.html

Find out its status
    Type:
        git status

Only app.js in red that means it is untracked and index.html is added and changes is commited

If you want to remove files from tracked
    Type:
        git reset

        or

        git rm --cached index.html

To add all types of html files:
        
        git add *.html

Add every file:
        
        git add.

Edit index file. Add to it body <p> New</p> and save file

Check out the status:

        git status

And index.html in red tell us that changes we now have at staging for commit

        git add .

        git status

Record changes to the repository (-m means message of changes)

        git-commit -m 'Initial Changes'     
        
Change app.js file 
    add to it   colsole.log("Hello Wir") and save

After check out it status
       
        git status 

And add it

        git add .

Record changes 

        git-commit -m 'Changes in app.js'

Create new file in the root. This excludes all files typed in from tracking of changes

        touch .gitignore

Create file with text "Error logs":

        touch log.txt

Go to the .gitignore and put there a file name and save it
        
        text log.txt

If we write down it will be added 
        
        git add .

Create two folders with files in it

        mkdir NewFolder

            create app1.js in it with text console.log(123)

        mkdir NewFolder2

            create app2.js in it with text console.log(123456)

Add to .gitignore /NewFolder2

Type and you will see only NewFolder added for commit:

        git add .

        git status
    
BRANCHES need if you working on the project with team

To create a branch:

        git branch login

Commit the changes:

        git commit -m 'New Change'

Change from master to login

        git checkout login

Create file login.html 

        touch login.html

and change it with text
        <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <meta http-equiv="X-UA-Compatible" content="ie=edge">
            <title>Document</title>
        </head>
        <body>
            Login
        </body>
        </html>

Change index.html. Add  <p> Login Form For WebApp</p> and save it.

Add  and commit it

        git add .
        git commit -m 'Changes in the Login'

Swith to master and you will see some files are gone

        git checkout master

To merge them

        git merge login -m 'Merging Login and Master'

Upload project to GitHub:

        Login to GitHub

        Create new repository

        Copy Link from github:
        git remote add origin https://github.com/.....

    Type:
        git remote
        #origin
    
    Upload your files:

        git push -u origin master

Create README.md file

        touch README.md

Type some text to there

Type:

        git add .

        git commit -m 'Added README.md'








