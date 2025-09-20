pipeline {
    agent {
        node {
            label 'roboshop-agent'
        }
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
                deleteDir()
            }
        }
    }

    post {
        always {
            echo "I will always say hello"
        }

        success {
            echo "I will say hello when the pipeline is success."
        }
    }

}