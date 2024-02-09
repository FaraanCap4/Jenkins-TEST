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
                sh 'mvn -nsu -Dhttp.port=8888 clean test'
            }
        }
        stage('Build main') {
            steps {
                echo 'Trigerring build on main branch'
                build 'main'
            }
        }
        stage('Build main') {
            steps {
                echo 'Trigerring build on main branch'
                build 'main'
            }
        }
    }
}
