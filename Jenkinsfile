pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
         git branch: 'main', url:  'https://github.com/AjinkyaP-09/simple-node-app.git'
      }
    }

    stage('Install Dependencies') {
      steps {
        sh 'npm install'
      }
    }

    stage('Run Tests') {
      steps {
        sh 'npm test'
      }
    }
  }

  post {
    always {
      echo 'Build complete!'
    }
  }
}
