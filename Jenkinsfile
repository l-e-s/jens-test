pipeline {
  agent {
    node {
      label 'dev3'
    }

  }
  stages {
    stage('Deploy') {
      steps {
        ws(dir: '/home/www/jenkins/${env.JOB_NAME}-${env.BUILD_NUMBER}') {
          dir(path: '/home/www/jenkins/${env.JOB_NAME}-${env.BUILD_NUMBER}') {
            sh 'pwd; ls'
          }

        }

        git(url: 'https://github.com/MIR24/FVOTE.git', branch: 'develop', changelog: true)
      }
    }
    stage('Inform') {
      steps {
        echo 'All done'
      }
    }
  }
}