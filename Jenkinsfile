pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from your GitHub repository
                script {
                    git 'https://github.com/himanshuhsk01/pipeline.git'
                }
            }
        }
        
        stage('Build') {
            steps {
                // Compile the Java code
                script {
                    sh 'javac Main.java'
                }
            }
        }
        
        stage('Test') {
            steps {
                // Run any tests if you have them
                script {
                    sh 'java Main'
                }
            }
        }
    }
    
    post {
        success {
            // This block will be executed if the pipeline is successful
            echo 'Build successful!'
        }
        
        failure {
            // This block will be executed if the pipeline fails
            echo 'Build failed!'
        }
    }
}
