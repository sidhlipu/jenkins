# Jenkins


# Minimum Hardware Requirements
256 MB of RAM
1 GB of drive space (although 10 GB is a recommended minimum if running Jenkins as a Docker container)


# Recommended hardware configuration for a small team:
4 GB+ of RAM
50 GB+ of drive space

# Installation of Java
```
sudo apt update
sudo apt install openjdk-11-jdk
java -version
```

# Installing Jenkins on Ubuntu
```
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null1
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
```

# Start Jenkins
```
sudo systemctl daemon-reload
sudo systemctl start jenkins
sudo systemctl status jenkins
```

# Post-installation
1. Browse to http://localhost:8080
2. From the Jenkins console log output, copy the automatically-generated alphanumeric password (between the 2 sets of asterisks).

or 
```
sudo cat /var/lib/jenkins/secrets/initialAdminPassword will print the password at console.
```

# Creating the first administrator user
When the Create First Admin User page appears, specify the details for your administrator user in the respective fields and click Save and Finish.

