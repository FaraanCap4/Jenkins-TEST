/* Requires the Docker Pipeline plugin */
pipeline {
    agent any//{ docker { image 'maven:3.9.6-eclipse-temurin-17-alpine' } }
    stages {
        stage('Chech Java Version') {
            java --version
        }
        stage('logs') {
            steps {
                echo "HELLO FROM JENKINSFILE"
            }
        }
    }
}
