pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''pwd
date'''
        echo 'test step'
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'test step'
          }
        }

        stage('test part') {
          steps {
            echo 'test par'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploy'
        sleep 13
      }
    }

  }
}