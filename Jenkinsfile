pipeline {
    agent {
        kubernetes {
            label 'jenkins-demo'
            containerTemplate {
                name 'test'
                image 'gcr.io/ipay-project/github-thusharaama-jenkins:c0506cff838a6e0ae93e3e50b0247ce142516ac7'
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
