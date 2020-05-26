pipeline {
    agent any 
    stages {
        stage('Build stage') { 
        
        steps  {
                withMaven (maven : 'maven_3.6.3') {
                sh 'mvn test'
                }
            }
            
            
        }
        stage('Test stage') { 
             steps  {
                withMaven (maven : 'maven_3.6.3') {
                sh 'mvn clean compile'
                }
            }
        }
        stage('Deploy') { 
            steps  {
                withMaven (maven : 'maven_3.6.3') {
                sh 'mvn deploy'
                }
            }
        }
    }
}