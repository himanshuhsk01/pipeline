node {
    try {
        stage('Checkout') {
            checkout scm
        }

        stage('Compile') {
            // Compile the Java application
            sh 'javac Main.java'
        }

        stage('Run') {
            // Run the compiled Java application
            sh 'java -cp . Main'
        }

        stage('Cleanup') {
            echo 'Doing some cleanup...'
        }
    } catch (Exception e) {
        // Handle exceptions if needed
        echo "Error: ${e.message}"
    }
}
