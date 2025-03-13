pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o output PES1UG22CS051-1.cpp && exit 1'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './output'  // Run the compiled binary
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
            echo 'Pipeline failed'
        }
    }
}
