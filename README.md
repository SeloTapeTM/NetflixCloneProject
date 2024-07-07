A system composed by the below containerized microservices:
Nginx as the HTTP engine .
NetflixFrontend as the frontend web app .
NetflixMovieCatalog and the movies catalog API .
Monitoring stack: Grafana, InfluxDB, availability test bash script.
The system is deployed in EC2 instances.
Communication is done via the Nginx with a real registered domain (using route53).
Simple CI/CD pipeline for the Nginx configuration file, and for build and deploy the NetflixMovieCatalog and the NetflixFrontend services using GitHub Actions .
