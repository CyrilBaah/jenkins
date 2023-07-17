pipeline {
  agent any

  tools {
    nodejs 'nodejs'
  }

  stages {
    stage('Verify Tools') {
      steps {
        // Verify the installation
        sh 'node --version'
        sh 'yarn --version'
        sh 'npm --version'
        sh 'node --version'
      }
    }

    stage('Clean Workspace') {
      steps {
        cleanWs()
      }
    }
  }

  post {
    always {
      echo 'One way or another, I have finished'
      cleanWs()
    }
  }
}
