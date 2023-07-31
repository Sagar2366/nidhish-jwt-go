pipeline {
    agent any 
    stages {
        stage('Verify java is installed or not') { 
            steps {
                sh "go version"
            }
            }
    
    stage('Build code') { 
            steps {
                sh "go mod tidy"
                sh 'go build -o main.go'
            }
            }
    }
}
