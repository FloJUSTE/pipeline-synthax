pipeline {
  agent any
  tools {
      maven 'mvn3'
  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn -Dmaven.test.failure.ignore=true install'
      }
      post {
        always {
            junit 'target/surefire-reports/**/*.xml'
        }
      }
    }
  }
}
