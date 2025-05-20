pipeline {
    agent any

    parameters {
        string(name: 'CREDENTIAL_ID', defaultValue: '012fe350-f90f-4b2a-887c-ad2d30150e16', description: 'Enter the Jenkins credential ID')
        booleanParam(name: 'USE_CREDENTIALS', defaultValue: true, description: 'Use the Jenkins credential ID')
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
                    if (params.USE_CREDENTIALS) {
                        withCredentials([usernamePassword(credentialsId: params.CREDENTIAL_ID, usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) {
                            echo "Deploying with user: $USERNAME"
                            // Actual deployment logic here
                        }
                    } else {
                        echo "exiting build due to  credential usage — USE_CREDENTIALS is false"
                        currentbuild.result= 'ABORTED'
                        retrun // exists pipeline here
                    }
                }
            }
        }
    }
}
