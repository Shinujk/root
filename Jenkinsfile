pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                // Checkout code from GitHub
                git branch: 'main', url: 'https://github.com/Shinujk/root/'
            }
        }

        stage('Run Bash Commands') {
            steps {
                // Run bash commands
                sh '''
                    echo "Hello, Jenkins!"
                    echo "Running bash commands from GitHub..."
                    ls -la
                    echo "Current directory: $(pwd)"
                '''
            }
        }

        stage('Display Results') {
            steps {
                // Display results
                sh '''
                    echo "Pipeline completed successfully!"
                '''
            }
        }
    }

    post {
        success {
            echo "Pipeline succeeded!"
        }
        failure {
            echo "Pipeline failed!"
        }
    }
}
