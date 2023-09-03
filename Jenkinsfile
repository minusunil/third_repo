pipeline {
    agent any
    stages {
        stage("build") {
            steps {
                echo "building....."
            }
        }
    }
    post {
        success {
            script {
                emailext(
                    subject: "Build Status Email",
                    body: "Build was successful",
                    to: "minunsunil@gmail.com",
                    attachLog: true  
                )
            }
        }
    }
}


