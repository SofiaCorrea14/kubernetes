#  Knote - Spring Boot App on Kubernetes

Este proyecto implementa una aplicación Spring Boot (Knote) desplegada en un clúster local de Kubernetes (Minikube).  
La aplicación utiliza MongoDB como base de datos y MinIO como servicio de almacenamiento, demostrando cómo ejecutar una aplicación stateless en contenedores Docker.



##  Tecnologías utilizadas
- Java 21 (OpenJDK)
- Spring Boot
- Docker
- Minikube / Kubernetes
- MongoDB
- MinIO
- Maven



##  Cómo ejecutar el proyecto localmente

1. **Clona este repositorio:**
   
   git clone https://github.com/SofiaCorrea14/kubernetes.git
   
   cd kubernetes

2. **Construye la imagen Docker:**
   
   docker build -t knote-app .

3. **Ejecuta Minikube y despliega los servicios:**

  minikube start
  kubectl apply -f mongodb-deployment.yaml
  kubectl apply -f minio-deployment.yaml
  kubectl apply -f knote-deployment.yaml

4. **Verifica que los pods estén en ejecución:**

   kubectl get pods

5. **Accede a la aplicación:**
   
   minikube service knote-service --url

   

 ## Imagen en Docker Hub

https://hub.docker.com/repository/docker/sofiac14/knote-app


## Autor

Sofía Correa Carmona



