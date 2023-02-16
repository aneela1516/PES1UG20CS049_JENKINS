pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o newfile newfile.cpp'
        build job: 'PES1UG20CS049-1'
      }
    }
    stage('Test') {
      steps {
        sh './newfile'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployment Successful'
      }
    }
  }
  
  post {
    failure {
        echo 'Pipeline failed'
    }
  }
}
