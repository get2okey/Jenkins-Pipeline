pipeline {

    agent any
    
    stages {
        stage('Build'){
            steps{
                echo "Building ..."
            }
            post{
                success {
                    mail to: "get2okey@gmail.com",
                    subject: "Build Status Email",
                    body: "Build was successful!"
                }
            }
        }
        stage('Test'){
            steps{
                echo "Unit tests"
                echo "Integration tests"
            }
        }
        stage('Code Analysis'){
            steps{
                echo "Check the quality of the code"
            }
        }
        stage('Security Scan'){
            steps{
                echo "Security Scannning"
            }
        }
        stage('Deploy to Staging'){
            steps{
                echo "Deploying to Staging"
            }
        }
        stage('Integration Tests on Staging'){
            steps{
                echo "Integration Tests on Staging"
            }
        }
        stage('Deploy to Production'){
            steps{
                echo "Deploy the code to the production server"
            }
        }

    }
}
