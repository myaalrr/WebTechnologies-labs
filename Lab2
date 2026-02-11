Part 1: Django web development framework
Task 1: install Django
Step 1: Once you have Python installed and PIP upgraded on your system, you must create a virtual
environment using 'python3 -m venv djangoenv'. This command will create an isolated Python
virtual environment for your development. You can do this anywhere, but it should not be in your local
git repository.

<img width="1379" height="243" alt="Image" src="https://github.com/user-attachments/assets/0ec7be3d-0620-45a9-a3d1-b076b0ba89f7" />


Step 2: Once the virtual environment is created, you should activate it. You do this by changing the
folder to the virtual environment you just created as follows:
> cd path_to_virtual_env/djangoenv
macOS: > source bin/activate
Windows: > Scripts\activate

<img width="1025" height="56" alt="Image" src="https://github.com/user-attachments/assets/9d1ebfcc-6c08-4ff4-ba58-c3dc2ce817c4" />
<img width="803" height="37" alt="Image" src="https://github.com/user-attachments/assets/ca07f668-e05f-4a21-a40f-ae87f32ad676" />


Step 3: once activated, we can now install Django
> pip install django

<img width="1241" height="564" alt="Image" src="https://github.com/user-attachments/assets/26ec379c-34f3-46a2-bcf1-4d94074ec287" />

Task 2: create, configure, and organize a new Django project
Step 1: Navigate to the desired location at which you will create the Django web application. For
example, 'DjangoProjects’ in your home folder.
> mkdir ~/DjangoProjects
> cd ~/DjangoProjects/

<img width="1220" height="370" alt="Image" src="https://github.com/user-attachments/assets/9e4e7236-ba45-4cbf-8b49-4188af992fc7" />

Step 2: Create your Django project as follows:
> Django-admin startproject libraryproject

<img width="1305" height="67" alt="Image" src="https://github.com/user-attachments/assets/57a46b7c-027c-4f52-b452-c433b5386179" />

Step 3: run the application to test that everything is working as intended:
> python manage.py runserver

<img width="1495" height="270" alt="Image" src="https://github.com/user-attachments/assets/91757c49-cd9c-43f1-b916-f414fb4617de" />

Step 4: Open your favorite internet browser and navigate to the localhost ‘http://127.0.0.1:8000/’. You
should see the Django default layout of the Django application.

<img width="1907" height="843" alt="Image" src="https://github.com/user-attachments/assets/fe6a6263-72eb-4706-9365-9c5e6b92b030" />

Task 3: configure your Django application
Throughout the lab sessions, the Django application will handle two services (sub-applications). This task
guides you in creating the appropriate structure for these two services. Hereafter, we will refer to the
ROOT folder as the folder that contains the manage.py file.
Step 1: Create some folders in the ROOT folder
> mkdir apps/ apps/template/ apps/static/

<img width="900" height="670" alt="Image" src="https://github.com/user-attachments/assets/74ca538e-5d98-472f-83f1-18880b7db864" />

Step 2: create two module services in the apps folder: bookmodule and usermodule
> cd apps
> python ../manage.py startapp bookmodule
> python ../manage.py startapp usermodule
These commands create two folders inside of the apps folder, and each one has a list of files as follows:
├── __init__.py
├── admin.py
├── apps.py
├── migrations
│ └── __init__.py
├── models.py
├── tests.py
└── views.py

<img width="1269" height="68" alt="Image" src="https://github.com/user-attachments/assets/0d23aca6-e029-49d1-b468-a22ed4c78657" />

Step 3: Open the files modules configuration files.
Open the file apps/bookmodule/apps.py and update the module name:
name = 'apps.bookmodule'
Do the same for the usermodule at apps/usermodule/apps.py
name = 'apps.usermodule'

<img width="869" height="194" alt="Image" src="https://github.com/user-attachments/assets/19588b79-1fc0-4edb-a9c7-182f7a87f730" />

<img width="1016" height="259" alt="Image" src="https://github.com/user-attachments/assets/0e1c82d4-4387-43ef-98db-a1fbc8b70292" />

Step 4: Update the Django application settings at ROOT/libraryproject/settings.py, and add the
following to the INSTALLED_APPS array.
INSTALLED_APPS = [
...,
'apps.bookmodule',
'apps.usermodule',
]

<img width="939" height="309" alt="Image" src="https://github.com/user-attachments/assets/a1d4690a-dc23-4ee7-a947-d64e9c0d552b" />

Step 5: run the server to test that everything works as intended. From the ROOT location of your Django
project, do the following:
> python manage.py runserver

<img width="1562" height="264" alt="Image" src="https://github.com/user-attachments/assets/19164cdd-7500-44c6-a877-a7068a6b6561" />

Part 2: Git system and connect your online repo with a local repo
Task 1: Create a local git repo.
Step 1: navigate to the ROOT folder of your Django application
> cd ~/DjangoProjects/libraryproject
Step 2: initialize your local Git repository:
> git init
(this command will create a git folder)

<img width="1566" height="478" alt="Image" src="https://github.com/user-attachments/assets/c6100acb-3469-4ec4-ac91-5f5610332daa" />
Step 3: You don’t want to add all the files from your local repository to the online one. So, create an
ignore file to add all file extensions that the git system will overlook.

macOS: > touch .gitignore & open .gitignore
Windows: > type NUL > .gitignore & .gitignore
Once the file .gitignore is opened in a text editor, add the following lines:
*.log
*.pot
*.pyc
__pycache__
*.bak
*.py[cod]
*$py.class
pip-log.txt
pip-delete-this-directory.txt
.ipynb_checkpoints
.python-version
celerybeat-schedule.*
# Environments
.env
.venv
env/
venv/
ENV/
env.bak/
venv.bak/
.mypy_cache/
**/migrations
*.DS_Store
**/__pycache__
**/.DS_Store
.history
Then, we need to stage the ignore file and let Git know about it.
> git add .gitignore
> git commit -m "add ignore file"
<img width="1212" height="61" alt="Image" src="https://github.com/user-attachments/assets/ce3c6fe6-e8f6-4219-953b-c0173a6d73a6" />
<img width="817" height="626" alt="Image" src="https://github.com/user-attachments/assets/6bccb9dc-244a-4181-9f81-fcde7e2257a3" />

<img width="1664" height="171" alt="Image" src="https://github.com/user-attachments/assets/d2a608d7-4060-4bf0-ad4a-191625cee6a3" />

Task 2: connect your local repository with the remote repository you created in Lab 2.
Step 1: before you can do anything, we must first configure git to use the SSH connection with your
remote repository. Use the same credentials that you used to create your online repository. Then, you
should do the following:
> git config --global user.name "Pixel"
> git config --global user.email "pixel@webmail.com"

<img width="1650" height="54" alt="Image" src="https://github.com/user-attachments/assets/afd8bc26-ac54-40fa-901e-c2572ea331c8" />

<img width="1345" height="85" alt="Image" src="https://github.com/user-attachments/assets/782dd383-b9fa-4816-b80d-bf567d05dab2" />

Step 2: Generate the authentication keys. You can visit this link for different operating systems, here we
use macOS compatibility commands.
> ssh-keygen -t ed25519 -C "pixel@webmail.com"
You will be prompted to enter the key's location. Press the enter/return key on your keyboard to accept
the default location, or you must give the full path to your SSH configuration folder.
> Enter a file in which to save the key(/Users/Pixel/.ssh/id_ed25519):[Press enter]
Then, you will be prompted to enter a passphrase. If you don’t want to set it up, you can press the
enter/return key anyway.

<img width="1409" height="578" alt="Image" src="https://github.com/user-attachments/assets/5e078666-680a-42ef-aea4-25b2c3573e6a" />

Step 3: Add the key to ssh-agent
> eval "$(ssh-agent -s)"

<img width="1220" height="332" alt="Image" src="https://github.com/user-attachments/assets/3f46715c-4bff-42de-8c77-c6f49d51f120" />

Step 4: Navigate to the online git repository and copy the project link you dedicated to this module. For
example, if your repository project is hosted on GitHub, then it should have this pattern:
https://github.com/<user_name>/<repo_name>.git

<img width="1739" height="432" alt="Image" src="https://github.com/user-attachments/assets/c6b4f2f9-2618-4ffe-a616-0b6be1008446" />

Step 4: Add your remote repository to your local git repository:
> git remote add origin https://github.com/<user_name>/<repo_name>.git

<img width="1210" height="132" alt="Image" src="https://github.com/user-attachments/assets/d7097a32-9132-4480-bc38-7025e0eb45e4" />

Step 5: Determine which branch your repository project has. Usually, it is called main. Then to the
following:
> git fetch origin
> git push -u origin main

<img width="1081" height="160" alt="Image" src="https://github.com/user-attachments/assets/01a19ee8-13fb-4aa9-b3cb-df844570a21f" />

Step 6: Double-check your content is successfully uploaded by visiting your remote online repository.

<img width="1380" height="544" alt="Image" src="https://github.com/user-attachments/assets/9311fbfb-0ecd-498c-ad7f-30e923f34234" />
