pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
            }
        }
        stage('Development') {
            when {
                branch 'dev'
            }
            steps {
                echo 'Deploying to development environment...'
                // Simulated deployment step
                echo 'Deployed to Development successfully.'
            }
        }
        stage('Test') {
            when{
                branch 'test'
            }
            steps {
                echo 'Running tests for Test branch...'
               
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
