pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Compiling the C++ source code...'
                build 'PES1UG22CS392-1'
                sh 'g++ file.cpp -o output'
            }
        }

        stage('Test') {
            steps {
                echo 'Running the compiled application...'
                sh './output' 
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed! Please check the logs.'
        }
        success {
            echo 'Pipeline executed successfully!'
        }
    }
}