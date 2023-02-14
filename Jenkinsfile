pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS670 PES1UG20CS670.cpp'
                build job: 'PES1UG20CSE670-1'
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG20CS670'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Success'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
