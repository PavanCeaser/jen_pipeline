pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/PavanCeaser/jen_pipeline.git'
            }
        }

        stage('Build') {
            steps {
                sh 'python3 -m venv venv'
                sh 'source venv/bin/activate && pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                sh 'source venv/bin/activate && python -m unittest tests/test_main.py'
            }
        }

        stage('Deploy') {
            steps {
                // Add your deployment steps here, e.g., using scripts or plugins
                sh 'echo "Deploying to production..."'
            }
        }
    }
}
