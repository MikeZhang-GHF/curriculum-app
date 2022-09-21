pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/MikeZhang-GHF/curriculum-app', branch: 'dev')
      }
    }

    stage('') {
      steps {
        sh 'ls -al'
      }
    }

  }
}