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
        stage('Deploy on premises') {
            steps{
                echo 'Deploying on premises using mvn clean deploy -DmuleDeploy -DskipMunitTests'
                sh 'mvn clean deploy -DmuleDeploy -DskipMunitTests'
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
