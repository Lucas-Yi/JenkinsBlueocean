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
            echo 'Building...'
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
