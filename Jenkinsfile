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
        stage('Deploy on premises') {
            steps{
                echo 'Moving packaged application to apps directory'
                sh 'cp "/home/faraan/.jenkins/jobs/MyPipeline/branches/main/workspace/target/jenkins-test-1.0.0-SNAPSHOT-mule-application.jar" /home/faraan/mule-enterprise-standalone-4.5.2/apps/jenkins-test.jar'
            }
        }
    }
}
