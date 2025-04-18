# Java Maven Build with Jenkins

This project demonstrates a basic CI/CD pipeline using Jenkins to build a simple Java application with Maven.

## 💻 Tech Stack
- Java (JDK 8 or 11)
- Maven
- Jenkins (via Docker)
- Git
- AWS EC2 (optional deployment environment)

## 📁 Project Structure

- `src/main/java/com/example/HelloWorld.java`: Main Java class
- `pom.xml`: Maven build file

## 🚀 How to Build with Jenkins

1. Create the ec2 instance
    ![Screenshot 2025-04-18 151526](https://github.com/user-attachments/assets/44e1890d-28b2-4a9f-86db-e4f76954f485)

2. Install Docker 
3. Start Jenkins:  
   `docker run -p 8080:8080 jenkins/jenkins:lts`
4. Install Maven inside Jenkins or set it up under Global Tool Configuration
5. Create a Freestyle job:
   - GitHub repo as source
   - Build step: `mvn clean package`
6. Add Post-build action to archive `target/*.jar`

## ✅ Sample Output
![Screenshot 2025-04-18 151717](https://github.com/user-attachments/assets/8cb3088c-adba-462c-8d25-6f5eb24731af)



