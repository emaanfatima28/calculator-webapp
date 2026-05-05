pipeline {
    agent any
    tools {
        maven 'Maven'
    }
    stages {
        stage('Clone') {
            steps {
                echo 'Cloning repository...'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package -DskipTests'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy to Tomcat') {
            steps {
                sh 'cp target/calculator.war C:/Users/Emaan/Downloads/apache-tomcat-11.0.21-windows-x64/apache-tomcat-11.0.21/webapps/'
            }
        }
    }
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}