pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                 git url: 'https://github.com/projectsquad02/Hotel-Management-System.git', branch: 'development'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package -DskipTests=true'
            }
        }
        stage('Deploy Docker Compose') {
            steps {
                sh 'docker-compose up'
            }
        }
    }
}
