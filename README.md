# IBM Full Stack Capstone Project
This is an IBM Full Stack Capstone Project. This full stack web application was built using HTML/CSS/BootStrap/React for the front-end. Python/Django/SQLite back-end to handle user management and views. Python/Flask/NLTK for sentiment analysis of reviewes. Node.js/Express/MongoDB handling dealership and reviews. Deployment using Docker, Kubernetes and IBM Cloud Engine.
Admin/Superuser privileges and functionalities were added to manage database of users and the inventory and management of vehicles. 

## Step 1: Cloning the Repository
```bash
git clone https://github.com/B-Phan/IBM-fullstack_developer_capstone_project.git
```

## Step 2: Setting up the Back-end and Virtual Environment
```bash
cd /home/project/IBM-fullstack_developer_capstone_project/server

pip install virtualenv
virtualenv djangoenv
source djangoenv/bin/activate

python3 -m pip install -U -r requirements.txt

python3 manage.py makemigrations

python3 manage.py migrate
```
## Step 3: Setting up the Front-end (Client-Side)
```bash
cd /home/project/IBM-fullstack_developer_capstone_project/server/frontend
npm install
npm run build
```


