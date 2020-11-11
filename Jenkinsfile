
pipeline {
    agent any
     
    stages {
      stage('checkout') {
           steps {
             
                git 'https://github.com/sruthiyelti/my-app.git'
          }
        }
        stage('code'){
            steps {
                withSonarQubeEnv(credentialsId: 'jenkins-sonar', installationName: 'sonar') {
                sh 'mvn package sonar:sonar'
                }
   }
       }
           }
}
