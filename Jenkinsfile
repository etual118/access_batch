pipeline {
  agent any
  stages {
    stage('getRaw') {
      steps {
        sh 'python /home1/irteam/user/load.py'
      }
    }
    stage('parseRaw') {
      steps {
        sh 'sh "/home1/irteam/user/daily_login_statistics/parse.sh"'
      }
    }
    stage('sendEmail') {
      steps {
        sh 'sh "/home1/irteam/user/daily_login_statistics/mailing.sh"'
      }
    }
  }
}
