# Eva DevOps Challenge

This repository contains a NodeJS web server which:

- Listens on the port specified by the PORT env variable or 3000 by default.
- Contains a single endpoint: `GET /api -> 200`
- Returns a JSON payload with a random chance of error (status code 500) and/or a delay.
- Logs to STDOUT in JSON format:

```
{"level":30,"time":1566421521743,"pid":2997,"hostname":"MacBook-Pro.local","reqId":60,"req":{"method":"GET","url":"/api","hostname":"localhost:3000","remoteAddress":"127.0.0.1","remotePort":53371},"msg":"incoming request","v":1}
{"level":30,"time":1566421527224,"pid":2997,"hostname":"MacBook-Pro.local","reqId":60,"res":{"statusCode":500},"responseTime":5480.768921997398,"msg":"request completed","v":1}
```

## Your mission, should you choose to accept it

- Clone this repo and create a repo of your own (DO NOT FORK THIS REPO).
- Dockerize the application.
- Create a simple CI/CD (use any service) pipeline which deploys the application on every commit to master.
- The app should be deployed to AWS in a scalable and production ready manner.
- The AWS infrastructure should be built using IaC.
- Make the logs searchable without ssh-ing into the server.
- Create a simple dashboard (use any service) where metrics about the server are shown.
- Alerts should be emitted for 500 responses and delivered via email to fernando.lopez@evatech.co with the subject `{{YOUR_NAME}} | 500 Response`.
