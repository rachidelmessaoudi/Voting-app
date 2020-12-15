# Voting-app
<p>voting-app is an application based on the microservices architecture and DevOps methodology. to create this application we used git, Docker, Jenkins, Kubernetes. It allows everyone to vote for their preferred candidate, to change their vote if they feel they are wrong, as well as to see the number of votes cast and the approval rating of each candidate.</p>
<h1>Architecture</h1>
This application consists of 5 microservices:

* Voting-app : web application developed in python (Flask Framework) which lets you vote between two options
* Redis : queue which collects new votes
* Worker : which consumes votes and stores them in database
* Postgresql : database backed by a Docker volume
* Result-app : webapp which shows the results of the voting in real time



<h1>Voting Interface </h1>



<h1>Voting Interface </h1>



<h1>Result Interface</h1>



<h1>Getting started</h1>

<p>Download and install Docker Desktop for Mac or Windows. Docker Compose will be automatically installed. On Linux, install Docker and docker compose.</p>

<h1>Run the application </h1>

<p>If you're using Docker Desktop on Windows, you can run the Linux version by switching to Linux containers

Run in this directory:</p>

`docker-compose up`

