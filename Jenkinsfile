pipeline {

agent { node { label 'Linux-Demo' } }
tools {
        maven 'maven3.3.9' 
        jdk 'jdk1.8'
    }
stages {
    stage('Run in parallel') {
     parallel {
        stage('Code validate') {
            steps {
                sh 'mvn validate'
            }
        }
        stage('Code Compile') {
            steps {
                sh 'mvn compile'
            }
        }
     }
    }
        stage('Code Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Code Package') {
            steps {
                sh 'mvn package'
            }
        }

        
    }
}