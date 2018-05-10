pipeline {
  agent {
    docker {
      args '-p 3000:3000'
      image 'gcr.io/google-containers/ubuntu:14.04'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
  }
}