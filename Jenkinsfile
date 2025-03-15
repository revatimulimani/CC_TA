pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building C++ Project...'
                    sh 'g++ -o PES2UG23CS818 nonexistent_file.cpp' // Replace with your actual file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running Tests...'
                    sh './PES2UG23CS818'  // Execute compiled file
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying the application...'
                    sh 'echo "Deployment successful!"'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed! Please check the logs for errors.'
        }
    }
}
