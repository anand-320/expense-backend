pipeline {
  agent {
    node {
      label 'ci-server'
    }
  }

  stages{

    stage('lint code'){
      when {
        allof {
          not { buildingTag() }
          branch 'main'
        }
      }
      steps {
        sh 'env'
        echo 'lint code'
      }
    }

    stage('Run unit test'){
      when { not { buildingTag() } }
      steps {
        echo 'Run unit test'
      }
    }

    stage('Run integration test'){
      when { not { buildingTag() } }
      steps {
        echo 'Run integration test'
      }
    }

    stage('Sonar scan code review'){
      when {
        allof {
          not { buildingTag() }
          branch 'main'
        }
      }
      steps {
        echo 'Sonar scan'
      }
    }

    stage('Build Code'){
      when { buildingTag() }
      steps {
        echo 'Build Code'
      }

    stage('Release software'){
      when { buildingTag() }
      steps {
        echo 'Release software'
      }
    }

  }
}