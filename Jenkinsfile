pipeline{
  agent any
  tools {
    maven 'Maven' 
  }
 environment {
    ANYPOINT = credentials('ANYPOINT')
 }
 stages {
 	stage ('Build'){
 		steps {
		
 				bat 'mvn package install'
 			
 		}
 	}
 	stage ('Deploy'){
 		steps {
 				bat 'mvn  package deploy  -Dusername=MSIJENKIN -Dpassword=MYnoki@523@ -Denvironment=Development -DmuleDeploy'
 			
 		}
 	}
 }

}
