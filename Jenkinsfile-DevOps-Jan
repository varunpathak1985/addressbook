pipeline {
    agent {
        node: 
          label 'alok-server'
     }
    tools {

        maven 'mymaven'
        jdk 'myjava'
    }
    stages {
        stage('Check Maven Version') {
            steps {
                sh 'mvn --version'
            }
        }
        stage('Check Java Version') {
            steps {
                sh 'java -version'
            }
        }
        stage('Validate the code') {
            steps {
                sh 'mvn validate'
            }
        }
         stage('Compile the code') {
            steps {
                sh 'mvn compile'
            }
        }
         stage('Test the code') {
            steps {
                sh 'mvn test'
            }
        }
        stage('package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
