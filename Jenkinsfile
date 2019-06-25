pipeline {
   agent any
   stages {
       stage('source code'){
           steps{
               checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/Anbunavan1/PetClinic.git']]])
           }
       }
       stage('compile'){
           steps{
               sh'/opt/apache-maven-3.6.1/bin/mvn compile'
           }   
       }
       stage('test'){
           steps{
               sh'/opt/apache-maven-3.6.1/bin/mvn test'
           }   
       }
       stage('package'){
           steps{
               sh'/opt/apache-maven-3.6.1/bin/mvn package'
           }   
       }
       
   }
}
