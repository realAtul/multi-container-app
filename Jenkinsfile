pipeline {
  agent any

  environment {
    COMPOSE_PROJECT_NAME = 'multi-app'
  }

  stages {
    stage('Clone Repo') {
      steps {
        git 'https://github.com/realatul/multi-container-app.git'
      }
    }

    stage('Build Docker Images') {
      steps {
        sh 'docker-compose build'
      }
    }

    stage('Deploy App') {
      steps {
        sh 'docker-compose up -d'
      }
    }
  }
}
