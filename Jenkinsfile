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
        stage ('Deploying the project') {
            steps {sh 'sudo scp -i /home/ec2-user/keyfile.pem /var/lib/jenkins/workspace/GitConnect_War-Repos_main/target/artifactid.war ec2-user@172.31.0.33:/usr/share/tomcat/webapps'}
        }
    }
}