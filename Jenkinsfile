pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the C++ project...'
                    sh 'g++ -o PES2UG22CS442-1 main.cpp' // Compile the C++ file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running the test...'
                    sh './PES2UG22CS442-1' // Execute the compiled C++ file
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying the application...'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
