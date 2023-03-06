pipeline {
  agent any
  stages {
    stage('checkout code') {
      steps {
        git(url: 'https://github.com/TrippleA-Ashaba/CI_CD.git', branch: 'dev')
      }
    }

    stage('log') {
      steps {
        sh 'ls -la'
      }
    }

    stage('build image') {
      steps {
        sh 'docker build . -t trippleaunit/calc-dev:$BUILD_NUMBER'
      }
    }

  }
}