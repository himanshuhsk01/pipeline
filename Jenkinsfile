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
                    bat(script: 'javac Main.java', returnStatus: true) // Use 'bat' on Windows
                    
                }
            }
        }
        
        stage('Test') {
            steps {
                // Run any tests if you have them
                script {
                    bat(script: 'java Main', returnStatus: true) // Use 'bat' on Windows
                    
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
