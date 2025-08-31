# :rocket: simple-java-docker :rocket:
---
## A simple java app that runs on docker :whale:
---
### Make & Change Dir :file_folder:
```bash
mkdir simple-java-docker && cd simple-java-docker/
```
---
## Get Clone This Repo From GitHub, Below Link:

⭐ [Clone GitHub Repo](https://github.com/LondheShubham153/simple-java-docker.git)
---
### :file_folder:List This Dir.
```bash
ls -ltrh
```
---
### :whale:Make Docker File:
- **vim Dockerfile** →→ `For Copy & Compile We Need Only Main.java File`
```bash
# stable official Java runtime base image
FROM openjdk:17-jdk-alpine

# metadata
LABEL maintainer="example-mail@gmail.com"
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
### Build An Dockerfile :whale: 
```bash
docker build -t java-app .
```

> ### Run as Cont 📦
```bash
docker run java-app
```

## 📂 Project Structure
css
Copy code
```
my-project/
├── src/
│   ├── main.py
│   ├── utils.py
│   └── __init__.py
├── tests/
│   └── test_main.py
├── docs/
│   └── README.md
├── requirements.txt
└── README.md
```
