# Django ToDo List Application

This project is an advanced to-do list web application with the basic features of most web apps, such as accounts/login, API, and interactive UI. 
To complete this task, you will need:

- CSS | [Skeleton](http://getskeleton.com/)
- JS  | [jQuery](https://jquery.com/)

## Getting Started

To begin, install the necessary requirements. Please note that these commands are compatible with Python 3.8 and higher due to the use of Django 4:

```
pip install -r requirements.txt
```

Next, create a database schema:

```
python manage.py migrate
```

Finally, start the server (default is <http://localhost:8000>):

```
python manage.py runserver
```

You can now explore the [API](http://localhost:8000/api/) or start on the [landing page](http://localhost:8000/).

## Task Description

The task is to extend a GitHub Actions workflow for this project by adding a Docker build and push to the DockerHub Registry. The requirements for this task are as follows:

1. The upload of the previous job's artifact should only be executed from the `main` branch.
2. Add a `docker-ci` job to the workflow.
3. The new job should only be executed from the `main` branch.
4. The job should include the following steps:
    1. Login to the DockerHub Registry.
    2. Build and Push a Docker image to your existing DockerHub Registry. The image should be tagged with the current commit's hash.
    3. Use the provided Dockerfile to build the image.
5. Store DockerHub credentials using GitHub Repository Secrets.
6. Create a pull request with the changes.
7. The description of the pull request should contain a reference to a workflow run with a successful Docker CI job.
