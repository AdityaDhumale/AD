4Th program

step1:Download Eclipse IDE for Java Developers. It is developed by the CLOUDS Lab organization and is written entirely in Java so we would need a Java IDE to simulate a cloud scenario using CloudSim.

step2:Download the CloudSim 3.0.3 zip file from GitHub and extract the folders within a folder in our computer storage.

step3:Download Apache Commons Math 3.6.1 zip file. It is required as it provides a faster, more accurate, portable alternative to the regular Math and StrictMath classes for large-scale computation in java files.

step4:Open Eclipse IDE and create a new Java Project

step5:The above-mentioned Java Project should be created with the location of the previously downloaded and extracted CloudSim 3.0.3 folder.

step6:The JAR file from the extracted Apache Commons Math 3.6.1 folder needs to be added to the JAR files of CloudSim.
Now the CloudSim Environment has been setup in the Eclipse IDE.

---------------------------------------------------------------------------------------------------------------------------------------

GOOGLE APP ENGINE
STEP 1 — Create GitHub Repository and Folders
1.	Open GitHub → New Repository 
2.	Name: web-app-engine 
Create files and folders using Add file → Create new file
Create this structure:
Web_app/
   app.yaml
   main.py
   requirements.txt
   templates/
       index.html
-	Paste the code (given below) into respective files and Commit.
STEP 2 — Open Google Cloud Console
1.	Go to: https://console.cloud.google.com 
2.	Create New Project 
3.	Enable It.
STEP 3 — Enable App Engine Admin API
1.	≡ Menu → APIs & Services → Library 
2.	Search App Engine Admin API 
3.	Click Enable 
4.	If asked → Authorize
STEP 4 — Open Cloud Shell (Shield / Square Icon)
Look at top-right corner
You will see:
[ >_ ]
First time:
•	Click Authorize / Enable 
•	Wait for terminal to start 
Then click:
Open Editor
STEP 5 — Create App Engine using command
In terminal:
gcloud app create
-	Select region
-	App Engine is created
STEP 6 — Clone GitHub Project
git clone https://github.com/your-username/web-app-engine.git
cd web-app-engine/Web_app
STEP 7 — Run Project
python main.py
STEP 8 — View Web Page
Click:
Web Preview 🌐 → Preview on port 8080
Output:
Success! Your Python-powered HTML is running.	
STEP 9 — Stop Server
fuser -k 8080/tcp
STEP 10 — Deploy to App Engine
gcloud app deploy
Press Y
Then:
gcloud app browse




CODE to be used
app.yaml
runtime: python39
entrypoint: gunicorn -b :$PORT main:app

main.py
from flask import Flask, render_template

app = Flask(_name_)

@app.route('/')
def home():
    return render_template('index.html', title="Home Page")

if _name_ == '_main_':
    app.run(host='127.0.0.1', port=8080, debug=True)

requirements.txt
flask==3.0.0
gunicorn==21.2.0

templates/index.html
<!DOCTYPE html>
<html>
<head>
    <title>{{ title }}</title>
</head>
<body>
    <h1>Success! Your Python-powered HTML is running.</h1>
</body>
</html>


---------------------------------------------------------------------------------------------


1st PROGRAM

step1:In D-drive navigate to Ubuntu NS2
step2:enter the admin password and click on install
step3:click on next ,yes and install
step4:in Ubuntu click on the new to create your own VM and name it.
step5: set the base memory>5000mb and select no of CPUS you want(usually 3)
step6:CHOOSE "use inbuilt VM" and click the folder icon beside it and go to the d-Drive .select Ubuntu and the file you created apperars there choose it.
step7:after choosing ,click on the next and finish ,your VM will be visible in Ubuntu
step8:click on setting ,go to display ,keep video memory>50mb,monitor count=3 and click on finish
step9: click on "start" and run a simple c program to check if everything is installed


#include <stdio.h>

int main() {
    int n, i;
    int a = 0, b = 1, next;

    printf("Enter number of terms: ");
    scanf("%d", &n);

    printf("Fibonacci Series:\n");

    for(i = 0; i < n; i++) {
        printf("%d ", a);
        next = a + b;
        a = b;
        b = next;
    }

    return 0;
}

-----------------------------------------------------------------------------------------------------------


1.git config --global user.name "ajaylight"
2.git config --global user.email "ajaylightyagami@gmail.com"
3.git config --global core.editor "code --wait"
4.code
5.git config --global -e
6.git config --global core.autocrlf true
7.mkdir repo1
8.cd repo1
9.git init
10.ls
11.git status
12.echo "HELLO GIT" >file.txt
13.git add file.txt
14.git commit -m "FIrst commit"
15.git remote add origin https://github.com/your-username/repo-name.git     //add local repo to git

16.git push -u origin master    //push
17.git pull origin master         //pull
18. git clone https/.......       //clone
19.git fetch               //fetch
20.git checkout -b newbranch             //creates and switches to new branch
21.git reset --hard HEAD~1          //reset (removes last commit completely
22.git branch -d newbranch             //delete
