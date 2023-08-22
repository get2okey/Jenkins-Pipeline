pipeline {

    agent any
    
    stages {
        stage('Build'){
            steps{
                echo "Building ..."
            }
        }
        stage('Test'){
            steps{
                echo "Unit tests"
                echo "Integration tests"
            }
            post{
                success {
                    mail to: "get2okey@gmail.com",
                    subject: "Test Status Email",
                    body: "Test was successful!"
                }
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
            post{
                success {
                    mail to: "get2okey@gmail.com",
                    subject: "Security Scan Status Email",
                    body: "Security scan was successful!"
                }
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
