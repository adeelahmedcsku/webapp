pipeline {   
agent any
environment{
MAVEN_HOME='/root/maven/apache-maven-3.5.3'
}
stages {  
 stage('Build') {  
 steps {  
 sh "${MAVEN_HOME}/bin/mvn clean package"  
    }  
 }
 
 stage (‘Deploy_WebApp’) {
            steps {
              sh 'scp target/*.war devops@10.0.2.15:~/tomcat/webapps/'
            }
        }

 
 
 } 
}
