pipeline {
    agent any

    environment {
        // You can define environment variables here, if needed
        PROJECT_NAME = 'MyProject'
        BUILD_DIR = 'build'
    }

    stages {
        // Stage 1: Checkout the source code from GitHub
        stage('Checkout') {
            steps {
                echo 'Checking out the code from GitHub...'
                git 'https://github.com/Samvardhani/Jenkins.git' // Change to your GitHub repo URL
            }
        }

        // Stage 2: Build the project
        stage('Build') {
            steps {
                echo 'Building the project...'
                script {
                    // Add your build commands here, like Maven, Gradle, npm, etc.
                    sh 'echo "Building project..."'  // Replace with your actual build command
                }
            }
        }

        // Stage 3: Test the project
        stage('Test') {
            steps {
                echo 'Running tests...'
                script {
                    // Add your test commands here
                    sh 'echo "Running tests..."'  // Replace with your actual test command
                }
            }
        }

        // Stage 4: Deploy the project
        stage('Deploy') {
            steps {
                echo 'Deploying the project...'
                script {
                    // Add your deploy commands here, like FTP, SSH, etc.
                    sh 'echo "Deploying project..."'  // Replace with your actual deploy command
                }
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed. Please check the logs.'
        }
    }
}
