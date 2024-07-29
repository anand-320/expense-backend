pipeline {
  agent {
    node {
      label 'ci-server'
    }
  }

  stages{

    stage('lint code'){
      steps {
        sh 'env'
        echo 'lint code'
      }
    }

    stage('Run unit test'){
      steps {
        echo 'Run unit test'
      }
    }

    stage('Run integration test'){
      steps {
        echo 'Run integration test'
      }
    }

    stage('Sonar scan code review'){
      steps {
        echo 'Sonar scan'
      }
    }

    stage('Release software'){
      steps {
        echo 'Release software'
      }
    }

  }
}