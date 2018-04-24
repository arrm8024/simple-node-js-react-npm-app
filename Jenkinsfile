pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3014:3000' 
        }
    }
    enviroment {
        CI = 'true'
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}
