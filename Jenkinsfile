pipeline {
 agent any
 stages {
 stage('Checkout') { steps { git 'https://github.com/hainunki-a11y/devops-practical-2026' } }
 stage('Build') { steps { sh 'python src/app.py' } }
 stage('Test') { steps { sh 'python -m pytest tests/' } }
 stage('Deploy') { steps { sh 'bash deploy.sh' } }
 }
}