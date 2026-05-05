pipeline {
    agent any
    tools {
        maven 'Maven'
    }
    stages {
        stage('Build') {
            steps {
                bat 'mvn clean package -DskipTests'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
        stage('Deploy to Tomcat') {
            steps {
                bat 'copy target\\calculator.war C:\\Users\\Emaan\\Downloads\\apache-tomcat-11.0.21-windows-x64\\apache-tomcat-11.0.21\\webapps\\'
            }
        }
    }
    post {
        success { echo 'Deployed successfully!' }
        failure { echo 'Build failed!' }
    }
}