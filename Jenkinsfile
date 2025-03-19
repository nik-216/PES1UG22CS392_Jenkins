pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Compiling the C++ source code...'
                sh 'g++ -o PES1UG22CS392-1 PES1UG22CS392.cpp'
            }
        }

        stage('Test') {
            steps {
                echo 'Running the compiled application...'
                sh './PES1UG22CS392-1' 
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