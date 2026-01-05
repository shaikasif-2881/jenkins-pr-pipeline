pipeline {
    agent any

    stages {

        stage('Job-1: Lint') {
            steps {
                sh 'python3 --version'
            }
        }

        stage('Job-2: Test') {
            steps {
                sh '''
                pip3 install pytest
                python3 -m pytest
                '''
            }
        }

        stage('Job-3: Build') {
            steps {
                sh 'python3 app.py'
            }
        }
    }
}
