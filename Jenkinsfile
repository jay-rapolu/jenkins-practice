pipeline {
    agent {
        label 'roboshop-agent'
    }

    options {
        timeout(time: 30, unit: 'MINUTES')
    }

    stages {
        stage('Build') {
            steps {
                script {
                    echo "Building..."

                }
            }
        }
        stage('Test') {
            steps {
                script {
                    echo "Testing..."
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    echo "Deploying..."
                }
            }
        }
    }

}