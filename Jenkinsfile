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
                    emailext attachLog: true, attachmentsPattern: 'generatedLogFile.txt',
                    to: "get2okey@gmail.com",
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
                    emailext attachLog: true, attachmentsPattern: 'generatedLogFile.txt',
                    to: "get2okey@gmail.com",
                    subject: "Security Scan Status Email",
                    body: "Security scan was successful!"
                }
            }
        }
        stage('Deploy to Staging'){
            steps{
                echo "Deploying the application to a staging server AWS EC2 instance"
            }
        }
        stage('Integration Tests on Staging'){
            steps{
                echo "Running integration tests on staging"
            }
        }
        stage('Deploy to Production'){
            steps{
                echo "Deploying the code to the production server AWS EC2 instance"
            }
        }

    }
}
