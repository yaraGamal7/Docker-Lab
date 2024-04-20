# ITI - Docker Lab 🐋

## Task 1: Working with Docker Hello-world Image
### Objective
Learn how to run a container using the hello-world image and manage containers and images.

### Steps
#### 1. Run a Container with hello-world Image
```bash 
docker pull hello-world
docker run hello-world

```
#### 2. Check Container Status and Explain
```bash
docker ps -a
```
#### 3. Start the Stopped Container
```bash
docker start mystic_einstein
```
#### 4. Remove the Container
```bash
docker rm charming_banzai
```
#### 5. Remove the Image
```bash
docker rmi -f hello-world
```
---

## Task 2: Running Container with Ubuntu Image
### Objective
Run an Ubuntu container in interactive mode, create a file inside it, and manage containers.

### Steps
#### 1. Run Ubuntu Container in Interactive Mode
```bash
docker pull ubuntu
docker run -it ubuntu
```
#### 2. Create a File inside the Container
```bash
touch file-yaraOs
```
#### 3. Stop and Remove the Container
```bash
docker stop serene_wilson
docker rm serene_wilson
```
#### 4. Check File Status
```bash
ls file-yaraOs
```
#### 5. What happened to hello-docker file?
```bash
already removed it with the container
```
#### 6. Remove All Stopped Containers
```bash
docker container prune
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
touch index.html
vi home.html
<!DOCTYPE html>                                                               
  1 <html lang="en">                                                              
  2 <head>                                                                        
  3     <meta charset="UTF-8">
  4     <meta name="viewport" content="width=device-width, initial-scale=1.0">
  5     <title>Yara jamal open source</title>
  6 </head>
  7 <body>
  8     <h1>Welcome </h1>
  9     <p>Yara jamal mahmoud </p>
 10 </body>
 11 </html>
 12 
```
#### 2. Write Dockerfile and Copy the HTML file to the Docker Image
```bash
vi Dockerfile
```
#### 3. Run Container with New Image
```bash
docker build -t custom-nginx .
```

#### 4. Test the Container, open your browser and navigate to http://localhost:8088 to check if everything is okay
```bash
docker run -d -p 8080:80 custom-nginx
```

