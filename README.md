# :rocket: simple-java-docker :rocket:
---
## A simple java app that runs on docker :whale:
---
### Make & Change Dir :file_folder:
```bash
mkdir simple-java-docker && cd simple-java-docker/
```
---
### Get GitHub Repo:
```bash
git clone https://github.com/LondheShubham153/simple-java-docker.git
```
---
:file_folder:List This Dir.
```bash
ls -ltrh
```
---
:whale:Make Docker File:
- **vim Dockerfile** →→ `Copy & Compile k liye sirf Main.java chahiye`
```bash
# stable official Java runtime base image
FROM openjdk:17-jdk-alpine

# metadata
LABEL maintainer="saadgeeus123@gmail.com"
LABEL version="1.0"
LABEL description="A simple Java application"

# working directory
WORKDIR /app

# Copy source code into the container
COPY src/Main.java /app/Main.java

# Compile the Java code
RUN javac Main.java

# Run the Java application when the container starts
CMD ["java", "Main"]
```
`ESC` `wq:` Enter
- docker build -t java-app .

> Run as Cont 📦
```bash
docker run java-app
```

