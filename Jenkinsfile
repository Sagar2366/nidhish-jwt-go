pipeline {
    agent any 
    stages {
        stage('Verify java is installed or not') { 
            steps {
                sh "go version"
            }
            }
    
    /*stage('Build code') { 
            steps {
                sh "go mod tidy"
                sh 'go build -o main.go'
            }
            }*/

    stage('Build docker image') { 
            steps {
                    sh 'sudo docker build -t go-image .'     
	                echo 'Build Image Completed'
                    sh 'docker images'
                }
        }
    }
}
