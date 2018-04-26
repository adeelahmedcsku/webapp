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
 
 stage ('Deploy_WebApp') {
            steps {
              sh 'scp -P 2222 target/*.war vagrant@10.4.40.77:/home/vagrant/tomcat/apache-tomcat-9.0.6/webapps/'
            }
        }

 
 
 } 
}
