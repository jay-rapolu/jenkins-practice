pipeline {
    agent {
        node {
            label 'roboshop-agent'
        }
    }

    environment {
        COURSE = "jenkins"
    }

    options {
        timeout(time: 30, unit: 'MINUTES')
    }

    stages {
        stage('Build') {
            steps {
                script {
                    echo "Building..."
                    printenv
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