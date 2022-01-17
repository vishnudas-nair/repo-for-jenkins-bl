pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''pwd
date'''
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'test-step'
          }
        }

        stage('test-parallel') {
          steps {
            echo 'test-is-paraelly-running'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Build has been deployed'
      }
    }

  }
}