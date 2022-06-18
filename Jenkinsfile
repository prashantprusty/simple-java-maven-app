pipeline { 
agent any tools { maven 'mymaven' } 
    stages { stage("Checkout") {
        steps {
git url: 'https://github.com/akshu20791/simplilearnjavaproject.git'

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
    stage("Unit test") {               
        steps {       
            bat "mvn test"               
           }
    }
       stage("package") {               
        steps {       
            bat "mvn package"               
           }
       }
} }
