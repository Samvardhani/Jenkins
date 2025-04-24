pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/Samvardhani/Jenkins.git'  // Clone your GitHub repository
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'  // Install dependencies (for Node.js)
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'  // Build your app (adjust as needed)
            }
        }

        stage('Archive Artifacts') {
            steps {
                archiveArtifacts artifacts: 'build/**', followSymlinks: false  // Archive build output
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy step placeholder'  // Placeholder for deployment logic
            }
        }
    }

    post {
        success {
            echo '✅ Build succeeded!'
        }
        failure {
            echo '❌ Build failed.'
        }
    }
}
