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
                python3 -m venv venv
                . venv/bin/activate
                pip install --upgrade pip
                pip install pytest
                pytest
                '''
            }
        }

        stage('Job-3: Build') {
            steps {
                sh '''
                python3 app.py
                '''
            }
        }
    }
}
