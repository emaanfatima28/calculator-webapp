# Calculator Web App

A simple Java-based calculator web application deployed on Apache Tomcat.

## Project Overview

This is a basic web calculator application built using Java (Servlet/JSP) and deployed on Tomcat.  
The application performs standard arithmetic operations through a web interface.

## Project Structure

- `Calculator/` → Extracted web application folder (for development)
- `Calculator.war` → Deployable WAR file
- `webapps/` → Deployment directory in Tomcat

## Deployment

1. Place the following inside your Tomcat `webapps` folder:
   - `Calculator/` OR
   - `Calculator.war`

2. Start Tomcat:

startup.bat


3. Open in browser:

http://localhost:8081/Calculator/


## Access URL


http://localhost:8081/Calculator/


## 🛠️ Tech Stack

- Java (Servlets/JSP)
- HTML/CSS
- Apache Tomcat

##  Notes

- The application is already deployed and working on port **8081**.
- No additional build steps (like Maven/Gradle) are required for running the current version.
- Either WAR or extracted folder works — avoid keeping both to prevent conflicts.

## 📷 Features

- Basic arithmetic operations:
  - Addition
  - Subtraction
  - Multiplication
  - Division
