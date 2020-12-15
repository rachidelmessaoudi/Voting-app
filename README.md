# Voting-app
<p>voting-app is an application based on the microservices architecture and DevOps methodology. to create this application we used git, Docker, Jenkins, Kubernetes. It allows everyone to vote for their preferred candidate, to change their vote if they feel they are wrong, as well as to see the number of votes cast and the approval rating of each candidate.</p>
<h1>Architecture</h1>
This application consists of 5 microservices:

* Voting-app : web application developed in python (Flask Framework) which lets you vote between two options
* Redis : queue which collects new votes
* Worker : which consumes votes and stores them in database
* Postgresql : database backed by a Docker volume
* Result-app : webapp which shows the results of the voting in real time

![l'architecture de l'application](https://user-images.githubusercontent.com/55992425/102250544-f9015d00-3f03-11eb-9510-1542ef2fa8a8.PNG)

![structur de lapp](https://user-images.githubusercontent.com/55992425/102249967-3ca79700-3f03-11eb-99da-48ff265857b2.PNG)


<h1>Voting Interface </h1>

![l'interface du vote](https://user-images.githubusercontent.com/55992425/102250609-09193c80-3f04-11eb-9e5b-d813cf6dbb13.PNG)

<h1>Result Interface</h1>

![Resultat des votes](https://user-images.githubusercontent.com/55992425/102250789-47aef700-3f04-11eb-846e-093903c883f4.PNG)

<h1>Getting started</h1>

<p>Download and install Docker Desktop for Mac or Windows. Docker Compose will be automatically installed. On Linux, install Docker and docker compose.</p>

<h1>Run the application </h1>

<p>If you're using Docker Desktop on Windows, you can run the Linux version by switching to Linux containers

Run in this directory:</p>

`docker-compose up`

