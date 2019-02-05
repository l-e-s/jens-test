pipeline {
  agent any
  stages {
    stage('Prepare') {
      steps {
        node(label: 'dev3') {
          ws(dir: "/home/www/jenkins/${env.JOB_NAME}/${env.BUILD_NUMBER}") {
            sh 'pwd; ls'
          }

        }

        sh 'echo "2nd step"; pwd; ls'
      }
    }
  }
}
