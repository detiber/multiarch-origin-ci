pipeline {
  agent any
  stages {
    stage('Checkout Project Repos') {
      steps {
        ansiColor('xterm') {
          timestamps {
            sh 'mkdir -p origin'
            dir(path: 'origin') {
              git(url: 'https://github.com/openshift/origin.git', branch: 'master')
            }
          }
        }
      }
    }
    stage('Build') {
      steps {
        echo 'Build'
        sh '''ls
ls origin'''
      }
    }
    stage('Test') {
      steps {
        echo 'Test'
      }
    }
    stage('Build RPMs and Images') {
      steps {
        echo 'Build RPMs and Images'
      }
    }
    stage('Extended Tests') {
      steps {
        echo 'Extended Tests'
      }
    }
    stage('Cleanup') {
      steps {
        cleanWs(cleanWhenAborted: true, cleanWhenFailure: true, cleanWhenNotBuilt: true, cleanWhenSuccess: true, cleanWhenUnstable: true, cleanupMatrixParent: true, deleteDirs: true)
      }
    }
  }
}
