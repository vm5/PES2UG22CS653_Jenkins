pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES2UG22CS653-1 hello.cpp' // Compile the .cpp file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES2UG22CS653-1' // Run the compiled binary
                }
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
            echo 'Pipeline Failed'
        }
    }
}
