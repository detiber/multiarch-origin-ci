pipeline {
  agent any
  stages {
    stage('Checkout Project Repos') {
      steps {
        sh 'mkdir -p ${WORKSPACE}/origin'
        dir(path: '${WORKSPACE}/origin') {
          git(url: 'https://github.com/openshift/origin.git', branch: 'master')
        }
        
      }
    }
    stage('Build') {
      steps {
        echo 'Build'
        sh '''ls
ls ${WORKSPACE}
ls ${WORKSPACE}/origin'''
      }
    }
  }
}