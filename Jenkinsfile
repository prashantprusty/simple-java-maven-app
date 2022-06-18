pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/prashantprusty/simple-java-maven-app.git'
            }
        }
        stage('compile') {
            steps {
                bat "mvn compile"  
            }
        }
        stage('review') {
            steps {
                bat "mvn pmd:pmd" 
            }
        }
		stage('Unit test') {
            steps {
                bat "mvn test" 
            }
        }
		stage('package') {
            steps {
                bat "mvn package"
		archiveArtifacts "target/*.jar"
            }
        }
    }
}
