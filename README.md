# coding-project-template
## Setup
Environment
```cd .\server\
pip install virtualenv
virtualenv djangoenv
.\djangoenv\Scripts\Activate  # for windows
source djangoenv/bin/activate # for Linux
pip install -U -r requirements.txt
```

## Static pages server start
Initial migrations
```
python3 manage.py makemigrations
python3 manage.py migrate
```

Create superuser
```
python3 manage.py createsuperuser
```

Run server
```
python3 manage.py runserver
```

## Django application start
```
cd .\frontend\
npm install
npm run build
```

## Docker build and start containers (app and DB)
```
cd .\database\
docker build . -t nodeapp
docker-compose up
```

## IBM Code Engine CLI. Deploy sentiment analysis on Code Engine as a microservice

In IBM Code Engine CLI:

```
cd fullstack_developer_capstone/server/djangoapp/microservices
docker build . -t us.icr.io/${SN_ICR_NAMESPACE}/senti_analyzer
docker push us.icr.io/${SN_ICR_NAMESPACE}/senti_analyzer
ibmcloud ce application create --name sentianalyzer --image us.icr.io/${SN_ICR_NAMESPACE}/senti_analyzer --registry-secret icr-secret --port 5000
```

check list of running applications
```
ibmcloud ce app list
```

## Git setup

```
git config --global user.email "vladimir.sokolenko@gmail.com" 
git config --global user.name "Vladimir Sokolenko"
```