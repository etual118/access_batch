pipeline {
  agent any
  stages {
    stage('getRaw') {
      steps {
        sh 'sh "/home1/irteam/user/daily_login_statistics/hivequery.sh"'
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