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
        bat(script: './jenkins/build.cmd', returnStdout: true)
      }
    }

    stage('Test Stage') {
      steps {
        bat(script: './jenkins/test.cmd', returnStdout: true)
      }
    }

  }
}