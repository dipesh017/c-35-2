pipeline {
  agent any
  stages {
    stage('Linux Testing') {
      parallel {
        stage('Linux Testing') {
          steps {
            sh 'echo linux Testing'
          }
        }

        stage('Windows Testing') {
          steps {
            sh 'echo windows Testing'
          }
        }

      }
    }

    stage('Build & Push') {
      steps {
        sh '''echo docker build -t name .
echo docker push'''
      }
    }

  }
  environment {
    ECS_CLUSTER = 'vote-app'
    ECS_REGION = 'us-east-1'
  }
}