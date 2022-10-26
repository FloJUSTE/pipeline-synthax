pipeline {
  agent any
  tools {
      maven 'Maven 3.3.9'
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
