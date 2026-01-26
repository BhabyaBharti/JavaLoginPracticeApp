# JavaLoginShowcase 🚀
This repository contains a sample login page implemented in Java for practicing Java deployment techniques. It includes a stylish and functional login UI, designed to help you understand how to deploy and manage a Java-based web application. 💻✨

![alt text](image.png)

## Features:
- User-friendly login interface 🖥️
- Responsive design 📱
- Sample code for deploying Java web applications 📦

## Purpose:
This project is a hands-on example for developers looking to practice deploying Java applications. It’s perfect for learning deployment strategies, UI design, and Java web development. 🎓🔧

## Branding:
Made with Love by **DevOps Insiders** ❤️. We are passionate about delivering high-quality solutions and resources for the DevOps community. 🌟

## Prerequisites:
Before you begin, ensure you have met the following requirements:

- **Java Development Kit (JDK)**: Ensure you have JDK 8 or higher installed. You can download it from [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) or use OpenJDK. ☕
- **Maven**: Apache Maven is used for building the project. Download and install Maven from [Maven's official website](https://maven.apache.org/download.cgi). 📦
- **Apache Tomcat**: A web server and servlet container for deploying the WAR file. Download it from [Apache Tomcat's website](https://tomcat.apache.org/download-90.cgi). 🖥️
- **Git**: Required for cloning the repository. Install Git from [Git's official website](https://git-scm.com/downloads). 🧩

## Getting Started:
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/JavaLoginShowcase.git
   ```
2. **Navigate to the Project Directory**:
   ```bash
   cd JavaLoginShowcase
   ```

## Deployment Instructions:
1. **Build the Project**:
   - Use Maven to clean and package the application into a WAR file:
     ```bash
     mvn clean package
     ```
   - This command will generate a WAR file in the `target` directory (e.g., `target/JavaLoginShowcase.war`). 📦

2. **Deploy to Tomcat**:
   - Copy the WAR file to the Tomcat `webapps` directory:
     ```bash
     cp target/JavaLoginShowcase.war $TOMCAT_HOME/webapps/
     ```
   - Restart the Tomcat server to deploy the WAR file:
     ```bash
     $TOMCAT_HOME/bin/shutdown.sh
     $TOMCAT_HOME/bin/startup.sh
     ```

3. **Access the Application**:
   - Once deployed, access the application through your web browser at:
     ```
     http://localhost:8080/JavaLoginShowcase
     ```

## Contributing:
Feel free to contribute by submitting issues or pull requests. We welcome any improvements or suggestions! 🤝

## License:
This project is licensed under the Apache License - see the [LICENSE](LICENSE) file for details. 📜

**DevOps Insiders** is committed to enhancing the DevOps community with valuable resources and examples. Follow us for more tools and insights! 🌟

### Emojis Reference:
- **🚀**: Represents the project being a showcase or launch.
- **💻✨**: Emphasizes the modern and functional nature of the login UI.
- **🖥️** and **📱**: Indicate the types of interfaces and design considerations.
- **🎓🔧**: Suggests learning and hands-on practice.
- **❤️** and **🌟**: Show love and commitment to quality from the DevOps Insiders community.
- **☕**: Represents Java.
- **📦**: Denotes Maven and deployment.
- **🧩**: Indicates Git.
- **🤝**: Encourages contributions.
- **📜**: Represents licensing.




# Java Application CI/CD Pipeline to Tomcat (Azure DevOps)

---

## 🚀 Purpose of This Repository

This repository demonstrates a **CI/CD pipeline for a Java (Maven) application**, with a focus on:

- Build and quality analysis
- Artifact packaging
- Automated deployment to a **Tomcat server running on a Virtual Machine**

> ⚠️ The application itself is intentionally simple.  
> 🎯 The primary focus is on **CI/CD pipeline design and deployment automation**.

---

## 🏗️ Technology Stack

- **Application:** Java (Maven, WAR packaging)
- **CI/CD:** Azure DevOps Pipelines
- **Code Quality:** SonarQube / SonarCloud
- **Deployment Target:** Tomcat on Linux VM (SSH-based deployment)

---

## 🔄 CI/CD Pipeline Overview

The pipeline follows a multi-stage structure:

### 1️⃣ Build & Quality Analysis
- Maven build (`clean verify`)
- SonarQube static code analysis
- Artifact packaging (WAR file)

### 2️⃣ Linting
- StyleLint for frontend/static assets (non-blocking)

### 3️⃣ Deployment
- Download build artifacts
- Install Tomcat (if not present)
- Deploy WAR file to Tomcat webapps directory
- Restart Tomcat service
- Verify application availability

---

## 🧩 Pipeline Highlights

✅ Multi-stage Azure DevOps pipeline  
✅ Artifact-based deployment strategy  
✅ VM deployment using SSH tasks  
✅ Separation of build and deploy concerns  
✅ Realistic VM-based delivery flow  

This mirrors how many **legacy and hybrid enterprise systems** are still deployed today.

---

## 🔐 Security Notes

- Secrets and tokens should be stored in **Azure DevOps secure variables or service connections**
- No credentials should be hardcoded in pipeline definitions

---

## 🎯 Why This Project Exists

This repository complements my other work focused on:
- Enterprise CI/CD pipelines
- Infrastructure as Code
- Cloud platform engineering

It represents **VM-based application delivery**, which remains relevant in many real-world environments.

---

## 👤 Author

**Bhabya Bharti**  
DevOps Engineer | CI/CD | Azure | DevSecOps
