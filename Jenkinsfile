/* Requires the Docker Pipeline plugin */
pipeline {
    agent any//{ docker { image 'maven:3.9.6-eclipse-temurin-17-alpine' } }
    stages {
        stage('Check Java Version') {
            steps {
                echo 'Checking Java Version'
                sh 'java --version'
            }
        }
    }
}
