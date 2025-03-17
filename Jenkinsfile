pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG22CS050-1 main.cpp'
                echo 'Build Stage Successful'
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG22CS000-1'
                echo 'Test Stage Successful'
            }
            post {
                always {
                    echo 'Test execution completed'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                echo 'Deployment Successful'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
