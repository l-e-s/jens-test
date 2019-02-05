pipeline {
  agent any
  stages {
    stage('Update code') {
      parallel {
        stage('Update code') {
          steps {
            node(label: 'dev3') {
              ws(dir: "${workdir}") {
                sh 'pwd; ls'
              }

            }

          }
        }
        stage('Update database') {
          steps {
            sh '''echo "create database $env.mysql_db" | mysql -uroot
ssh mir24-db mysqldump -uroot mir24 | mysql -uroot $env.mysql_db
'''
          }
        }
      }
    }
    stage('inform') {
      steps {
        echo 'Test done'
      }
    }
  }
  environment {
    workdir = '"/home/www/jenkins/${env.JOB_NAME}/${env.BUILD_NUMBER}"'
    mysql_db = '"mir24_jentest"'
  }
}