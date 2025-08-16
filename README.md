# Run a simple  Java Maven Build job in  Jenkins 

This is a simple *Java HelloWorld application* built with *Maven* and integrated with Jenkins.

## 📌 Project Overview
- A basic Java program that prints:

Hello, Jenkins + Maven!

- Configured with **Maven (pom.xml)** for build automation.
- Built and packaged in *Jenkins Freestyle Job* using mvn clean package.

---

## 🛠 Tools & Technologies
- *Java 21* (JDK)
- *Maven 3.x*
- *Jenkins (LTS via Docker)*
- *GitHub*

---

## 📂 Project Structure

hello-java-maven/ ├── src/ │   └── main/ │       └── java/ │           └── HelloWorld.java ├── pom.xml └── README.md

---

## ⚙ Jenkins Job Setup

1. *Start Jenkins*  
   ```bash
   docker run -p 8080:8080 jenkins/jenkins:lts

2. Configure Tools

Go to Manage Jenkins → Global Tool Configuration

Add JDK and Maven



3. Create Freestyle Job

New Item → Freestyle project → hello-java-maven

In Source Code Management, link this GitHub repo

In Build section → Invoke top-level Maven targets

Goal:

clean package



4. Build & Verify

Run job → Check Console Output

Expected result:

[INFO] BUILD SUCCESS





---

📦 Output

Maven generates a JAR file in:

target/hello-1.0.jar



---

📸 Screenshots

✅ Jenkins Job Configuration
![job](Screenshot6-png.png)
![job](Screenshot7-png.png)
![job](Screenshot8-png.png)
![job](Screenshot9-png.png)
✅ Console Output with BUILD SUCCESS
![hello](Screenshot10-png.png)
![hello ](Screenshot1-png.png)
![hello](Screenshot2-png.png)
![hello](Screenshot3-png.png)
![hello](Screenshot4-png.png)
✅ Generated hello-1.0.jar
![jar](Screenshot5-png.png)


---
