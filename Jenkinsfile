pipeline {
  agent any
  stages {
    stage('Allocate') {
      steps {
        node(label: 'dev19')
        ws(dir: 'test')
      }
    }
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