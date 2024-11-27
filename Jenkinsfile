pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                
                sh 'python3 -m venv venv'
                sh 'bash -c "source venv/bin/activate && pip install -r requirements.txt"'
            }
        }
        stage('Test') {
            steps {
                sh 'python -m unittest tests/test_main.py'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying to production...'
            }
        }
    }
}