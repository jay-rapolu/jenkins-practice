pipeline {
    agent {
        node {
            label 'roboshop-agent'
        }
    }

    environment {
        COURSE = "jenkins"
    }

    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    options {
        timeout(time: 30, unit: 'MINUTES')
        disableConcurrentBuilds()
    }

    stages {
        stage('Build') {
            steps {
                script {
                    echo "Building..."
                    sh 'printenv'
                    sleep 10
                }
            }
        }
        stage('Test') {
            input {
                message "should we continue to testing?"
                ok "yes, we should"
            }
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