pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                echo 'Checking out source code...'
                checkout scm
            }
        }
        stage('Install Dependencies') {
            steps {
                echo 'Installing dependencies...'
                sh 'npm install'
            }
        }
        stage('Build Application') {
            steps {
                echo 'Building the application...'
                sh 'npm run build'
            }
        }
        stage('Run Tests') {
            steps {
                echo 'Running tests...'
                sh 'npm test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh 'echo "Deployment successful!"'
            }
        }
    }
    post {
        success {
            echo '✅ Build succeeded!'
        }
        failure {
            echo '❌ Build failed! Check the logs.'
        }
    }
}

