
 pipeline {
     agent any
     environment {
          PATH="/opt/maven/bin:$PATH"
     }
     stages {
        stage ('build') { 
          steps {
            sh 'mvn clean install'

          }
        }  
        stage ('sonarqube analysis') {
          envirnoment {
            scannerhome= tool "sonarqube-server-scanner"
          }
          steps {
            with SonarQubeEnv ("sonarqube-server") {
              sh "${scannerhome}/bin/sonar-scanner"

            }
          }
        }  

     }
 }
