/* Requires the Docker Pipeline plugin */
pipeline {
    any agent //{ docker { image 'maven:3.9.6-eclipse-temurin-17-alpine' } }
    stages {
        stage('logs') {
            steps {
                echo "HELLO FROM JENKINSFILE"
            }
        }
    }
}
