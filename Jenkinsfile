pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/MikeZhang-GHF/curriculum-app', branch: 'dev')
      }
    }

    stage('Log') {
      steps {
        sh 'ls -al'
      }
    }

    stage('Build') {
      steps {
        sh 'docker build -f curriculum-front/Dockerfile .'
      }
    }

    stage('Log into Dockerhub') {
      environment {
        DOCKERHUB_USER = 'A'
        DOCKERHUB_PASSWORD = 'B'
      }
      steps {
        sh 'docker login -u $DOCKERHUB_USER -p $DOCKERHUB_PASSWORD'
      }
    }

    stage('Push') {
      steps {
        sh 'docker push '
      }
    }

  }
}