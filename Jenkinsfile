pipeline {
     agent any
     stages {
         stage('build step') {
              steps {
                 echo "Build stage is running"
              }
         }
     }
     post {
         always {
             echo "You can always see me"
         }
         success {
              echo "I am running because the job ran successfully"
         }
         unstable {
              echo "The build is unstable. Try fix it"
         }
         failure {
             echo "The build failed"
         }
     }
}
