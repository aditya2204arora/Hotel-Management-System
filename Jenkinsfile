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
                sh 'docker compose up -d'
            }
        }
        stage('SonarQube analysis') {
        steps {
            sh "mvn clean verify sonar:sonar -Dsonar.projectKey='Hotel-management' -Dsonar.host.url='http://20.246.95.180:9000' -Dsonar.login=sqa_68981035c032709be2e5f5def0ad5c323d8e524c" 
        }
        }
    }
}
