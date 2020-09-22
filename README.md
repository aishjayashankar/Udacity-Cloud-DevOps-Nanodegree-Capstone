# Udacity-Cloud-DevOps-Nanodegree-Capstone<br /><br />

# Prerequisites:<br />

Install Jenkins<br />
Install EKS<br />
Install Docker<br />
Create an account in dockerhub <br />
Add dockerhub credentials to Jenkins<br />
Add AWS Credentials to Jenkins<br /><br /><br />

# Steps to be followed:<br />
1. ./run_docker.sh (For the blue image from blue folder)<br />
2. ./upload_docker.sh (upload the blue image to docker hub)<br />
3. ./run_docker.sh (For the green image from green folder)<br />
4. ./upload_docker.sh (upload the green image to docker hub)<br />
5. Ensure EKS is running<br />
6. kubectl apply -f ./blue-controller.json (create replication controller for blue)<br />
7. kubectl apply -f ./green-controller.json (create replication controller for green)<br />
8. kubectl apply -f ./blue-green-service.json (create the service)<br />
9. kubectl get svc (Gives the LoadBalancer DNS for blue deployment)<br />
10. Update the service to redirect to green by changing the selector to app=green<br />
11. kubectl apply -f ./blue-green-service.json<br />
12. kubectl get svc (Gives the LoadBalancer DNS for green deployment)
