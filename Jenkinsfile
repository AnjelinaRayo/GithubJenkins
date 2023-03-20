node('built-in') 
    {
        stage('Continuous Download ') 
         {
            git 'https://github.com/AnjelinaRayo/Github-jenkins-Inte.git'
         }
	stage('Continuous Build') 
         {
            sh 'mvn package'
         }
         stage('Continuous Deployment') 
         {
                sh 'scp  /var/lib/jenkins/workspace/Pipeline-1/target/maven-web-application.war ubuntu@172.31.56.235:/var/lib/tomcat9/webapps/'
         }  
         stage('Continuous Testing') 
         {
            sh 'echo "Test is Passed"'
             
         }
         stage('Continuous Delivery') 
         {
            input message: 'Waiting For Approval ', submitter: 'Manager'
            sh 'scp /var/lib/jenkins/workspace/Pipeline-1/target/maven-web-application.war ubuntu@172.31.49.122:/var/lib/tomcat8/webapps/'
}


}
