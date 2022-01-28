DOCKER Intro:

Pipeline: script which can be isolated in a service container such as docker for data ingestion and proccess.

Docker structure: contains an SO, Python version, libraries, and other dependences such as postgres

We can run postgres in other container within the same computer

We can manage Postgres with other docker for PgAdmin 

Docker image is such an snapshot to set up an environment. We can run it later on AWS Batch, Kubernetes services in GCP...

Allows good CI CD (with jenkins github actions etc) such as making local integration tests

Hint for windows:

use MINGW for using linux commands on bash (linux like environment) Comes when you install gitbash

You can use linux subsytem for windows WSL

HANDS ON:

code . for opening vs code in the current path

docker run -ti container action Example:

docker run -ti ubuntu bash

Commands of docker:

docker run -it —entrypoint python:3.9    To overwrite the entrypoint (what is exactly computed when we run the container

The next time we create an image it doesnt contains what we installed via bash in an specific image. We need the dockerfile

After modyfing the docker file we need to build based on it. We need to specify some extra things such as t for name (docker build -t test creates it under test name) if we want to specify a version we can docker build -t test:pandasversion)

docker build -t test: