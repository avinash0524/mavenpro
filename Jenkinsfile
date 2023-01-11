pipeline {
  agent any
  stages {
    stage('clone') {
      steps {
        git 'https://github.com/avinash0524/mavenpro.git'
      }
    
    }
    stage('Build') {
steps{
    sh 'mvn clean package install'
}
  }
  stage('test') {
      steps{
          sh 'mvn test'
      }
  }
  stage('sonar') {
      steps{
          sh ''
      }
  }
  post{
        success {
            junit '**/target/surefire-reports/TEST-*.xml'
        }
  
  }
}
}
