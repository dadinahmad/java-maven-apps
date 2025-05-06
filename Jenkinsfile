pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                script {
                    echo "Testing the Application"
                    echo "Execution pipeline for branch"
                }
            }
        }

        stage('Build') {
            when {
                expression { env.BRANCH_NAME == 'main' } 
            }
            steps {
                script {
                    echo "Building the Application"
                }
            }
        }

        stage('Deploy') {
            when {
                expression { env.BRANCH_NAME == 'main' }
            }
            steps {
                script {
                    echo "Deploying the Application"
                }
            }
        }
    }
}
