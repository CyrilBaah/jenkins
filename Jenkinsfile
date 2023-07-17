pipeline {
    agent any

    tools { nodejs 'nodejs' }

    stages {
        // stage('SonarQube Analysis') {
        //     steps {
        //         withSonarQubeEnv('SonarQube') {
        //             script {
        //                 def scannerHome = tool 'SonarScanner'
        //                 sh "${scannerHome}/bin/sonar-scanner"
        //             }
        //         }
        //     }
        // }
        

         // Verify the installation
        sh 'yarn --version'
        sh 'npm --version'
        sh 'node --version'



        stage('Clean WS') {
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