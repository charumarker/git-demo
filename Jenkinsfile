pipeline {
    agent none
    stages {
        stage('Build') {
            agent {
                docker {
                    image 'python:3.5.1'
                }
            }
            steps {
                sh 'python -m py_compile car.py'
                stash(name: 'compiled-results', includes: '*.py*')
            }
        }
    }
}