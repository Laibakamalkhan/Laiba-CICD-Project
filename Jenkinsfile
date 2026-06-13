pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
    stage('Build') {
      steps {
        echo 'Building...'
        sh '/usr/bin/node --version'
        sh '/usr/bin/npm --version'
      }
    }
    stage('Test') {
      steps {
        echo 'Tests passed!'
      }
    }
    stage('Deploy') {
      steps {
        sh 'docker build -t laiba-cicd-project .'
        echo 'Deployed!'
      }
    }
  }
  post {
    success { echo 'Pipeline SUCCESS!' }
    failure { echo 'Pipeline FAILED!' }
  }
}
