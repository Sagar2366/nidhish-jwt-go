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
            def customImage = docker.build("go-image:${env.BUILD_ID}")

            customImage.inside {
                sh 'go mod tidy'
                }
                }
        }
    }
}
