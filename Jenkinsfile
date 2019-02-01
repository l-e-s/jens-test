pipeline {
  agent any
  stages {
    stage('Prepare') {
      steps {
        node(label: 'dev3')
        ws(dir: '/home/www/jenkins/env.JOB_NAME')
        sh 'pwd; ls'
      }
    }
  }
}