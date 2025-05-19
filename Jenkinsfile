pipeline {
               agent any


               parameters {
                string(name: 'ID', defaultvalule: '123', description: 'this is a string parameter')
                
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
                 stage("depoly"){
                                steps {
                                        echo 'this applciation is deploying..'
                                }
                 }
  }
}

