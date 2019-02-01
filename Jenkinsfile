pipeline {
  agent {
    node {
      label 'dev3'
    }

  }
  stages {
    stage('Deploy') {
      steps {
        ws(dir: '/home/www/jenkins/JOB_NAME@2') {
          dir(path: '/home/www/jenkins/JOB_NAME@2') {
            sh '''pwd; ls
'''
          }

        }

        git(url: 'https://github.com/MIR24/FVOTE.git', branch: 'dev-nv-1')
      }
    }
    stage('Inform') {
      steps {
        echo 'All done'
      }
    }
  }
}