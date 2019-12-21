pipeline
 {
  agent any
  stages{
     stage('Build Application'){
     steps{
     bat 'mvn clean install'
     }
     }
     
     stage('Depoy Application to Mulesoft CloudHub'){
     steps{
     bat 'mvn package deploy -DmuleDeploy'
     }
     }
     
     stage('Perform Regression Testing'){
     steps{
     bat 'newman run D:\\newman\\worldtimezone.postman_collection.json --disable-unicode'
     }
     }
   }
 }