pipeline {
  agent none
  stages {
    stage('Deploy app to development') {
      agent any
      when {
        branch 'Development'
      }
      steps {
        sh 'echo hello'
      }
    }

    stage('Deploy app to production') {
      agent any
      when {
        branch 'master'
      }
      steps {
        sh 'echo hello'
      }
    }

  }
  triggers {
    pollSCM('* * * * *')
  }
}