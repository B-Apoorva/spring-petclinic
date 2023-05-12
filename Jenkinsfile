pipeline{
agent any
stages{
   stage("Git Checkout"){
      steps{
       git branch: 'main', credentialsId: '8764ef1c-795f-46d4-882d-1fde8bcd6796', url: 'https://github.com/B-Apoorva/spring-petclinic.git'
           }
      }
stage("Maven Build"){
  steps{
  sh "mvn compile"
  sh "mvn test"
  sh "mvn clean package"
  sh "mv target/*.war target/petclinic.war"
       }
}
 
 }
}
