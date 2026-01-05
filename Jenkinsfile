pipeline {
    agent any

    stages {

        stage('Job-1: Lint') {
            steps {
                echo "Running lint checks"
                sh '''
                python3 --version
                '''
            }
        }

        stage('Job-2: Test') {
            steps {
                echo "Running tests"
                sh '''
                python3 -m pytest || exit 1
                '''
            }
        }

        stage('Job-3: Build') {
            steps {
                echo "Building application"
                sh '''
                python3 app.py
                '''
            }
        }
    }
}
