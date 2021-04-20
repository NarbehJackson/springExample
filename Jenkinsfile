pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean'
      }
    }
    stage('Deploy') {
      steps {
        sh 'mvn package'
      }
    }
  }
}
