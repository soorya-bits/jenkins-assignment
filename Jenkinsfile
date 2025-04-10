pipeline {
    agent any

    environment {
        STAGING_DIR = "/deploy/staging"
        PRODUCTION_DIR = "/deploy/production"
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'python3 -m py_compile app.py'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'pytest || true' // Simulated
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging...'
                sh 'bash scripts/deploy-staging.sh'
            }
        }

        stage('Deploy to Production') {
            steps {
                input "Deploy to production?"
                echo 'Deploying to production...'
                sh 'bash scripts/deploy-production.sh'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed. Please check logs.'
        }
    }
}