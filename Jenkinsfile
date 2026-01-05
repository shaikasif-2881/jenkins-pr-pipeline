pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo "Building application"
                python3 -m py_compile app.py
            }
        }

        stage('Test') {
            steps {
                echo "Running unit tests"
                python3 -m venv venv
                sh '. venv/bin/activate && pip install pytest && pytest'
            }
        }

        stage('Quality') {
            steps {
                echo "Running code quality checks"
                python3 -m py_compile app.py
            }
        }
    }

    post {
        always {
            echo "Pipeline completed for PR"
        }
    }
}
