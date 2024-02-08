pipeline {
    agent any
    environment{
        NAME = "test"
    }

    stages {
        stage('Checkout') {
            steps {
                // Check out the source code from your version control system
                echo "coucou ${env.NAME}"
            }
        }
    }
}

