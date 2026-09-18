pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/hainunki-a11y/devops-practical-2026'
      }
    }
    stage('Build') {
      steps {
        bat 'python src\\app.py'
      }
    }
    stage('Test') {
      steps {
        bat 'if exist tests\\ (python -m pytest tests) else (echo "No tests found; skipping pytest")'
      }
    }
    stage('Deploy') {
      steps {
        bat 'if exist deploy.bat (deploy.bat) else (echo "No deploy.bat found; skipping deploy")'
      }
    }
  }
}