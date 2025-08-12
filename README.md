Kubernetes Cluster with Minikube — Task 5

# Screenshots Drive URL : https://docs.google.com/document/d/1qevbkqjBtxQIDuLdaccK9UdANYX7vLLXZ3CtQTrXEPk/edit?usp=sharing

Steps & Commands

Kubernetes Cluster with Minikube — Task 5

I started Minikube using Docker driver
minikube start --driver=docker

I created the deployment file

I applied the deployment and checked pods
kubectl apply -f deployment.yaml
kubectl get pods -o wide

I created the service file

I applied the service and checked services
kubectl apply -f service.yaml
kubectl get svc

I accessed the application
minikube service nginx-service --url

I scaled the deployment
kubectl scale deployment nginx-deployment --replicas=4
kubectl get pods -o wide

I inspected pod details and logs
kubectl describe pod <pod-name>
kubectl logs <pod-name>

Finally, I cleaned up everything
kubectl delete -f service.yaml
kubectl delete -f deployment.yaml
minikube stop
minikube delete
