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

    }
}