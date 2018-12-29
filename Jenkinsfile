pipeline {
  agent any
  stages {
    stage('Deploy') {
      steps {
        git(url: 'https://github.com/l-e-s/jens-test.git', branch: 'master')
      }
    }
    stage('Inform') {
      steps {
        echo 'All done'
      }
    }
  }
}