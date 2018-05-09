pipeline {
    agent {
        kubernetes {
            label 'jenkins-demo'
            containerTemplate {
                name 'dind-jdk8-maven3'
                image 'eu.gcr.io/jenkins-demo/dind-jdk8-maven3:v4'
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
