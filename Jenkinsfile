pipeline {
  agent any

  tools {
    nodejs 'nodejs'
  }

  stages {
    stage('Install Dependencies') {
      steps {
        // Current directory
        sh 'pwd'


        // Install Yarn
        sh 'npm install -g yarn'

        // Install npm
        sh 'curl -L https://www.npmjs.com/install.sh | sh'
      }
    }

    stage('Verify Tools') {
      steps {
        // Verify the installation
        sh 'node --version'
        sh 'yarn --version'
        sh 'npm --version'
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
