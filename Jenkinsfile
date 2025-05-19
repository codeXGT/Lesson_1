pipeline {
               agent any


               parameters {
                string(name: 'ID', defaultvalue: '123', description: 'this is a string parameter')
                
               }

  stages {
              stage("build"){
                       steps {
                               echo 'building this application..'

                       }
              }
              stage("test"){
                        steps {
                                 echo 'testing this application..'
                        }
              }
                 stage("deploy"){
                                steps {
                                        echo 'this application is deploying..'
                                }
                 }
  }
}

