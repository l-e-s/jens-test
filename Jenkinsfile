pipeline {
  agent {
    node {
      label 'dev3'
    }

  }
  stages {
    stage('Deploy') {
      steps {
        ws(dir: '/home/www/dev19/JOB_NAME@2') {
          sh '''pwd; ls
'''
          git(url: 'https://github.com/l-e-s/jens-test.git', branch: 'master')
        }

      }
    }
    stage('Inform') {
      steps {
        echo 'All done'
      }
    }
  }
}