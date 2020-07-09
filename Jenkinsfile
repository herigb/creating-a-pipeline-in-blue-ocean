pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing'
        sh '''ls -l
chmod -R ugo+rwx jenkins && ./jenkins/scripts/test.sh'''
      }
    }

    stage('Delivery') {
      steps {
        echo 'Deploying'
        sh './jenkins/scripts/deliver.sh'
        input '\'Finished using the web site? (Click "Proceed" to continue)'
        sh './jenkins/scripts/kill.sh'
      }
    }

  }
  environment {
    CI = 'true'
  }
}