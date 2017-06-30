pipeline {
  agent any
  stages {
    stage('Checkout Project Repos') {
      steps {
        git(url: 'https://github.com/openshift/origin.git', branch: 'master')
      }
    }
    stage('Build') {
      steps {
        echo 'Build'
        sh 'ls'
      }
    }
  }
}