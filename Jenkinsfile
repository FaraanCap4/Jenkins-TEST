/* Requires the Docker Pipeline plugin */
pipeline {
    agent any//{ docker { image 'maven:3.9.6-eclipse-temurin-17-alpine' } }
    stages {
        stage('Check versions') {
            steps {
                echo 'Checking Java Version'
                sh 'java --version'
                echo 'Checking Maven Version'
                sh 'mvn --version'
            }
        }
        stage('Test project') {
            steps {
                echo 'Testing project using mvn -nsu clean test'
                sh 'mvn -nsu clean test'
            }
        }
        stage("Build project") {
            steps{
                echo 'Building project using mvn -nsu -DskipMunitTests clean package'
                sh 'mvn -nsu -DskipMunitTests clean package'
            }
        }
    }
}
