pipeline {
    agent any
    stages {
        stage ('Maven clean') {
            steps { sh 'mvn clean'}
        }
        stage ('Testing Maven') {
            steps {sh 'mvn test'}
        } 
        stage ('Building Maven') {
            steps {sh 'mvn package'}
        }  
    }
}