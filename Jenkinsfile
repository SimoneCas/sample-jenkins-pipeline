pipeline {
  agent any
  stages {
    stage('Start Pipeline') {
      agent any
      steps {
        echo 'Start Sample Pipeline'
        sh 'sleep 5'
        sh 'echo Success!'
      }
    }

    stage('Second Stage') {
      steps {
        sh 'echo Another Placeholder'
      }
    }

  }
}