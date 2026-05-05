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
                bat 'copy target\\calculator.war C:\\Users\\Emaan\\Downloads\\apache-tomcat-9.0.117\\webapps\\'
            }
        }
    }
    post {
        success { echo 'Deployed successfully!' }
        failure { echo 'Build failed!' }
    }
}