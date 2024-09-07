pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            when {
                branch 'Test'
            }
            steps {
                echo 'Running tests for Test branch...'
                
            }
        }

        stage('Development Deployment') {
            when {
                branch 'Development'
            }
            steps {
                echo 'Deploying to development environment...'
                // Simulated deployment step
                echo 'Deployed to Development successfully.'
            }
        }

        stage('Production Deployment') {
            when {
                branch 'main'
            }
            steps {
                echo 'Deploying to production environment...'
                // Simulated deployment step
                echo 'Deployed to Production successfully.'
            }
        }
    }

    post {
        always {
            echo 'Cleaning up workspace...'
            deleteDir()
        }
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
