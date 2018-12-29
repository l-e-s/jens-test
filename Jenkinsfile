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