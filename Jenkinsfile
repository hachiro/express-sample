pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('hello') {
      parallel {
        stage('hello') {
          steps {
            sh 'echo "hello"'
          }
        }
        stage('hello2') {
          steps {
            sh 'echo "hello2"'
          }
        }
      }
    }
  }
}