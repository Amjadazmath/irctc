
 pipeline {
     agent any
     environment {
          PATH="/opt/maven/bin:$PATH"
     }
     stages {
       stage ("git clone") {
         steps {
           git url: "https://github.com/Amjadazmath/irctc.git", "branch: main"


         }
       }
      
        stage ("build") { 
          steps {
            sh 'mvn clean install'

          }
        }  

     }
 }
