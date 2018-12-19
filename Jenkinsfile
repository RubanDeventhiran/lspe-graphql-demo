pipeline {
  agent any
  stages {
    stage('Git') {
      steps {
        git(poll: true, url: 'https://github.com/RubanDeventhiran/lspe-graphql-demo', branch: 'master')
      }
    }
    stage('Build') {
      agent {
        node {
          label 'kube'
        }

      }
      steps {
        sh 'uname -a'
      }
    }
  }
}
