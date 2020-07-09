pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
        sh 'sh \'npm install\''
      }
    }

    stage('Test') {
      steps {
        echo 'Testing'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying'
      }
    }

  }
}