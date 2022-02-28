pipeline {
  agent any
  stages {
    stage('prepare') {
      steps {
        echo 'helloworld'
        sleep 1
      }
    }

    stage('build') {
      parallel {
        stage('print') {
          steps {
            timestamps() {
              echo 'Helloworld Again'
            }

          }
        }

        stage('test') {
          steps {
            sh '''#!/bin/sh
# This is a comment!
echo Hello World'''
          }
        }

      }
    }

    stage('deploy') {
      steps {
        sleep 3
      }
    }

  }
}