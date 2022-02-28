pipeline {
  agent any
  stages {
    stage('prepare') {
      steps {
        echo 'helloworld'
        sleep 1
      }
    }
    stage('prepare1') {
      steps {
        withMaven(maven : 'apache-maven-3.6.1') {
            bat'mvn clean compile'
          }
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
            sh '''$ chmod a+rx my-script.sh
                  $ ./my-script.sh'''
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
