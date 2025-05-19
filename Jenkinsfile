pipeline {
    agent any

    parameters {
        string(name: 'ID', defaultValue: '', description: 'Enter the Jenkins credential ID')
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
