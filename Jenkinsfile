pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/szaher/freezer', branch: 'master', changelog: true)
      }
    }
    stage('Verify') {
      parallel {
        stage('Verify') {
          steps {
            sh 'ls -lh'
          }
        }
        stage('Verify2') {
          steps {
            sh 'pwd'
          }
        }
        stage('Verify3') {
          steps {
            echo 'Is it Ok ?'
          }
        }
      }
    }
    stage('Unit') {
      steps {
        sh 'python --version'
      }
    }
  }
}