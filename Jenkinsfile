pipeline {
  agent { docker { image 'maven:3.3.3' } }
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean'
      }
    }
    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }
    stage('Deploy') {
      steps {
        sh 'mvn package'
      }
    }
    stage('report') {
      steps {
        cucumber fileIncludePattern: '**/*.json', sortingMethod: 'ALPHABETICAL'
      }
    }
  }
}
