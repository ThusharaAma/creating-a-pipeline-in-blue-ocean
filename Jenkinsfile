pipeline {
    agent {
        kubernetes {
            label 'jenkins-demo'
            containerTemplate {
                name '6-alpine'
                image 'node:6-alpine'
                ttyEnabled true
                command 'cat'
            }
        }
    }
  stages {
    stage('Build') {
      agent {
        docker {
          image 'node:6-alpine'
          args '-p 3000:3000'
        }

      }
      steps {
        sh 'npm install'
      }
    }
  }
}
