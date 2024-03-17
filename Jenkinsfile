pipeline {
  agent any 
  stages {
    stage('Fetch Code') {
      steps {
        git branch: 'main', credentialsId: 'GitHubIsep', url: 'https://github.com/TiagoCastroIsep/devOpsRepo.git'
      }
    }

    stage('Build') {
      steps {
        sh 'echo "Build completed."'
      }
    }
  }

  post {
    always {
      sh 'echo "${currentBuild.currentResult}: Job ${env.JOB_NAME} build ${env.BUILD_NUMBER}"'
    }
  }
}
