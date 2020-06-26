# Lab: API Deployment

[Click here to connect to deployed site on MS Azure](http://52.247.232.82:8000/admin)
It will take some time for DNS resulation.

## Overview

It’s time to deploy!

First steps are to make sure your Application is able to run well in a remote environment.

Once you are confident that your Application is *deployable` then time to research deployment options.

## Feature Tasks and Requirements

- Modify your application to store SECRET_KEY, ALLOWED_HOSTS, DEBUG and DATABASE information in .env file.
- Add CORS capabilities to your app and whitelist allowed origins.
- All the code changes will be in settings.py so check the demo code for CORS and Env related lines.

## Deployment Requirements

- Research web hosting sites capable of working with Docker
- NOTE no money is required for this lab but you may choose to create a trial account.
  - But you are responsible for making sure you don’t hit with charges when trial is complete.

## Implementation Notes

- You are not required to use Poetry since the requirements.txt is being supplied.
- However if you run into issues with supplied requirements.txt then you are responsible for rebuilding.

## Useful Terminal Commands

```bash
docker-compose up --build
docker-compose down
docker-compose restart
docker-compose exec web ./manage.py migrate
docker-compose exec web ./manage.py collectstatic
```

## User Acceptance Tests

- Manually confirm API using Postman/HTTPie.
- Remember to use deployed url for postman requests.
