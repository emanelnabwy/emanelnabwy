pipeline {
    agent any
    stages {
        stage("run fortend") {
           steps {
              echo " execting yarn ......"
              nodejs ("node10.17") {
                   sh 'yarn install'
               }
               
           }   
         }
        stage("run backend") {
            steps {
               echo " execting gradle......"
               withGradle() {
                   sh './gradlew -v'
                }
            }    
            
         }
    }
}
