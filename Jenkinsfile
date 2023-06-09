pipeline {
    agent {
        docker {
            image 'node:lts-bullseye-slim' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Restore packages') {
            steps {
                echo "Building dotnet backend.."
                bat "dotnet restore ${workspace}\\TestBackendAPI\\TestBackendAPI.sln"
            }
        }
        stage('Build') {
            steps {
                echo "Building react user interface.."
                sh '''
                cd reactclientapp
                npm install
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                echo "Enter Test Protocols Here."
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "Enter Delivery Proticols Here."
                '''
            }
        }
    }
}
