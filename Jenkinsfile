pipeline {
   agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }
  stages {
    stage('Build') {
      steps {
         withEnv(['PATH+EXTRA=/usr/sbin:/usr/bin:/sbin:/bin']) {
            echo 'Building'
            sh 'npm install'
         }
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