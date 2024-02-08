pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Check out the source code from your version control system
                git 'https://github.com/Nyftheart/spring-demo.git'
            }
        }

        stage('Build') {
            steps {
                // Build the project using Maven
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                // Run tests using Maven
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                // Example: deploy the artifact to Nexus or any other repository manager
                sh 'mvn deploy'
            }
        }
    }

    post {
        success {
            // If the pipeline succeeds, send a notification or trigger another job
            echo 'Build successful! Send notifications...'
        }
        failure {
            // If the pipeline fails, send a notification or perform any cleanup tasks
            echo 'Build failed! Send notifications...'
        }
    }
}
