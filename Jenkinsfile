pipeline {
    agent {
        docker {image "node:16-alpine"}
    }
    
    stages {
        stage('code') {
            steps {
                checkout scm
            }
        }
    }
    
    stages {
        stage('test') {
            agent {
                docker {image 'python:latest'}
            }
            steps {
                sh 'python test.py'
            }
        }
    }
}
