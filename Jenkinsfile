pipeline {

  agent any

  tools {
    nodejs 'NodeJs'
  }

  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }

    stage('Install Dependency') {
      steps {
        sh "npm ci"
      }
    }

   stage('Build'){
     steps {
       sh "npm run build"
     }
   }
  }
}
