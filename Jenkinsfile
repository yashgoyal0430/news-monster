pipeline {

  agents any

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
        stash name: "jar-artifacts", includes: "target/*.jar"
      }
    }

   stage('Build'){
     steps {
       sh "npm run build"
     }
   }
  }
}
