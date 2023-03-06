pipeline {
  agent any
  stages {
    stage('checkout code') {
      steps {
        git 'https://github.com/TrippleA-Ashaba/CI_CD.git'
      }
    }

    stage('log') {
      steps {
        sh 'ls -la'
      }
    }

    stage('Build image') {
      steps {
        sh 'docker build . -t trippleaunit/test-app:$BUILD_NUMBER'
      }
    }

  }
}