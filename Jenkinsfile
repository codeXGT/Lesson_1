pipeline {
    agent any

    parameters {
        string(name: 'ID', defaultValue: '012fe350-f90f-4b2a-887c-ad2d30150e16', description: 'Enter the Jenkins credential ID')
        boolean(name: 'use-credentails', defaultValue: true, description: 'Use the Jenkins credential ID')
    
    }

    stages {
        stage("build") {
            steps {
                echo 'building this application...'
            }
        }

        stage("test") {
            steps {
                echo 'testing this application...'
            }
        }

        stage("deploy") {
            steps {
                script {
                    withCredentials([usernamePassword(credentialsId: params.ID, usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) {
                        echo "Deploying with user: $USERNAME"
                        // Here, use USERNAME and PASSWORD as needed
                    }
                }
            }
        }
    }
}
