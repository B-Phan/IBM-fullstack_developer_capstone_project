# IBM Full Stack Capstone Project
This is an IBM Full Stack Capstone Project that is to be completed at the end of the 10 courses provided in this certificate. This full stack web application was built using HTML/CSS/BootStrap/React for the front-end. Python/Django/SQLite back-end to handle user management and views. Python/Flask/NLTK for sentiment analysis of reviewes. Node.js/Express/MongoDB handling dealership and reviews. Deployment using Docker, Kubernetes and IBM Cloud Engine.
Admin/Superuser privileges and functionalities were added to manage database of users and the inventory and management of vehicles. 

## Step 1: Cloning the Repository in Terminal 1
```bash
git clone https://github.com/B-Phan/IBM-fullstack_developer_capstone_project.git
```

## Step 2: Setting up the Back-end and Virtual Environment in Terminal 1
```bash
cd /home/project/IBM-fullstack_developer_capstone_project/server

pip install virtualenv
virtualenv djangoenv
source djangoenv/bin/activate

python3 -m pip install -U -r requirements.txt 
python3 manage.py makemigrations
python3 manage.py migrate --run-syncdb
python3 manage.py runserver
```
## Step 3: Setting up the Front-end (Client-Side) in Terminal 2
```bash
cd /home/project/IBM-fullstack_developer_capstone_project/server/frontend
npm install
npm run build
```
## Step 4: Setting up the Code Engine in Terminal 3
```bash
cd IBM-fullstack_developer_capstone_project/server/djangoapp/microservices
docker build . -t us.icr.io/${SN_ICR_NAMESPACE}/senti_analyzer
docker push us.icr.io/${SN_ICR_NAMESPACE}/senti_analyzer
ibmcloud ce application create --name sentianalyzer --image us.icr.io/${SN_ICR_NAMESPACE}/senti_analyzer --registry-secret icr-secret --port 5000
```
## Step 5: Setting up the MongoDB database in Terminal 4
```bash
cd /home/project/IBM-fullstack_developer_capstone_project/server/database
docker build . -t nodeapp
docker-compose up
```

