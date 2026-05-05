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
                bat '''
                    call C:\\tomcat9\\bin\\shutdown.bat
                    timeout /t 5
                    copy /Y target\\calculator.war C:\\tomcat9\\webapps\\
                    call C:\\tomcat9\\bin\\startup.bat
                '''
            }
        }
    }
    post {
        success { echo 'Deployed successfully! Visit: http://localhost:8081/calculator/' }
        failure { echo 'Build failed!' }
    }
}