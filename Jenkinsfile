/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'maven:3.9.6-eclipse-temurin-17-alpine' } }
    stages {
        stage('logs') {
            steps {
                sh echo "HELLO FROM JENKINSFILE"
            }
        }
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}
