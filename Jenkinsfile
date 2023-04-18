pipeline {
    agent any

    environment {
        DIRECTORY_PATH = "C:/ProgramData/Jenkins/.jenkins/Jobs/"
        TESTING_ENVIRONMENT = "testing"
        PRODUCTION_ENVIRONMENT = "Axesh"
    }

    stages {
        stage('Build') {
            steps {
                echo "Fetching the source code from: ${DIRECTORY_PATH}"
                echo "Compiling the code and generating any necessary artifacts"
            }
        }

        stage('Test') {
            steps {
                echo "Testing unit tests"
                echo "Testing integration tests"
            }
        }

        stage('Code Quality Check') {
            steps {
                echo "Checking the quality of the code"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying the application to ${TESTING_ENVIRONMENT} environment"
            }
        }

        stage('Approval') {
            steps {
                echo "Waiting for approval..."
                sleep(time: 10, unit: 'SECONDS')
                echo "Approved"
            }
        }

        stage('Deploy to Production') {
            steps {
                echo "Deploying the application to ${PRODUCTION_ENVIRONMENT} environment"
            }
        }
    }
}
