pipeline {
  agent {
    node {
      label 'dev3'
    }

  }
  stages {
    stage('Deploy') {
      steps {
        ws(dir: '/home/www/jenkins/$JOB_NAME') {
          dir(path: '/home/www/jenkins/$JOB_NAME') {
            sh '''pwd; ls
'''
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