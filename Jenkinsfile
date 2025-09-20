pipeline {
    agent {
        label 'roboshop-agent'
    }

    options {
        timeout(time: 1, unit: 'SECONDS')
    }

    stages {
        stage('Build') {
            steps {
                script {
                    echo "Building..."
                    sleep 2
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