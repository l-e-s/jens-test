pipeline {
  agent any
  stages {
    stage('Prepare') {
      steps {
        ws(dir: '${ITEM_ROOTDIR}/builds/$JOB_NAME/$BUILD_NUMBER') {
          sh 'pwd; ls'
        }

      }
    }
  }
}