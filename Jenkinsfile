pipeline {
    agent any 
    stages {
        stage('Verify java is installed or not') { 
            steps {
                sh "go version"
            }
            }
        }
    stages {
        stage('Build code') { 
            steps {
                sh "go mod tidy"
                sh 'go . main.go'
            }
            }
        }
}
