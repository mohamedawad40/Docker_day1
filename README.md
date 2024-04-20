# ITI - Docker Lab 🐋

## Task 1: Working with Docker Hello-world Image
### Objective
Learn how to run a container using the hello-world image and manage containers and images.

### Steps
#### 1. Run a Container with hello-world Image
```bash
sudo docker run hello-world

```
#### 2. Check Container Status and Explain
```bash
docker ps -a
exit ,the container stoped after complete its tasks

```
#### 3. Start the Stopped Container
```bash
docker start peaceful_taussig
```
#### 4. Remove the Container
```bash
docker rm df6fe9d4f5b2

```
#### 5. Remove the Image
```bash
docker rm df6fe9d4f5b2
docker ps -a
docker rmi hello-world

```
---

## Task 2: Running Container with Ubuntu Image
### Objective
Run an Ubuntu container in interactive mode, create a file inside it, and manage containers.

### Steps
#### 1. Run Ubuntu Container in Interactive Mode
```bash

docker run -it ubuntu
```
#### 2. Create a File inside the Container
```bash
touch hello-docker
```
#### 3. Stop and Remove the Container
```bash
exit
docker ps -a
docker rm d1adbfb42c7f
```
#### 4. Check File Status
```bash

all files removed 
```
#### 5. What happened to hello-docker file?
```bash
all files removed
```
#### 6. Remove All Stopped Containers
```bash
for each container 
docker rm id
```
#### 7. Bonus: Remove All Containers in One Command
```bash

docker container prune -f
```

---
## Task 3: Creating a Custom Nginx Docker Image
### Objective
Create a custom Docker image using Nginx and a local HTML file.

### Steps
#### 1. Create a Local HTML File
```bash
nano index.html
```
#### 2. Write Dockerfile and Copy the HTML file to the Docker Image
```bash
docker pull nginx:alpine
nano Dockerfile

FROM nginx:alpine
COPY index.html /usr/share/nginx/html/index.html

docker build -t nginx-awad .



```
#### 3. Run Container with New Image
```bash
docker run -d -p 8088:80 nginx-awad

```

#### 4. Test the Container, open your browser and navigate to http://localhost:8088 to check if everything is okay

```bash

```
![myimage](https://github.com/mohamedawad40/Docker_day1/blob/main/Capture.JPG)
