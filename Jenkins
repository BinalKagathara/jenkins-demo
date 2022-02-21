pipeline {
    agent any 
    stages {
        stage('clone repo and clean') { 
            steps {
                bat "rd /s /q jenkins-demo"
                bat "git clone https://github.com/BinalKagathara/jenkins-demo.git"
                bat "mvn clean -f jenkins-demo"
            }
        }
        stage('Test') { 
            steps {
                bat "mvn test -f jenkins-demo" 
            }
        }
        stage('Deploy') { 
            steps {
                bat "mvn package -f jenkins-demo" 
            }
        }
    }
}
