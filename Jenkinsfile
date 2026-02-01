
pipeline {
    agent any
    stages {
        stage('Clone Code') {
            steps {
                // This pulls the code from the repo you are about to link
                checkout scm
            }
        }
        stage('Docker Build') {
            steps {
                // This builds an image using the Dockerfile in your repo
                bat 'docker build -t my-ai-app .'
            }
        }
        stage('Docker Run') {
            steps {
                // This runs the container to prove it works
                bat 'docker run --rm my-ai-app'
            }
        }
    }
}
