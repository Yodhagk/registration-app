pipeline {
    agent {label 'Jenkins-Agent'}
    tools {
        jdk 'java 17'
        maven 'Maven3'
          }
    stages {
        stage ("Cleanup Workspace") {
            steps {
                cleanWs()
            }
        }

        stage ("Checkout From SCM"){
            steps {
             git branch: 'main',credentialsId: 'github',url: 'https://github.com/Yodhagk/registration-app.git'
                }
        }
        stage("Build Application") {
            steps{
                sh "mvn clean package"
                 }
             }

           
    }

}