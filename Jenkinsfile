pipeline {
  agent any
  stages {
    stage('Start Pipeline') {
      agent any
      steps {
        echo 'Start Sample Pipeline'
        sleep 2
        echo 'Print after sleep'
      }
    }

    stage('Build Stage') {
      steps {
        bat(script: './build.cmd', returnStdout: true)
        archiveArtifacts(artifacts: 'target/*.jar', fingerprint: true)
      }
    }

    stage('Test Stage') {
      steps {
        junit '**/surefire-reports/**/*'
      }
    }

  }
}