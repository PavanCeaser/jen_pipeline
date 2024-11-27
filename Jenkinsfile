pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    
                    url: 'https://github.com/PavanCeaser/jen_pipeline.git'
            }
        }
        stage('Build') {
            steps {
                sh 'python3 -m venv venv'
                sh '/var/lib/jenkins/workspace/Python-pipeline/venv/bin/python -m pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                sh '/var/lib/jenkins/workspace/Python-pipeline/venv/bin/python -m unittest tests/test_main.py'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying to production...'
            }
        }
    }
}
