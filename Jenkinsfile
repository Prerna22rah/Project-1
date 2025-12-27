pipeline {
  agent any

  environment {
    IMAGE_NAME = "prernar22/devops-app"
    IMAGE_TAG  = "1.0"
  }

  stages {

    stage('Clone Code') {
      steps {
        git branch: 'main', url: 'https://github.com/Prerna22rah/Project-1'
      }
    }

    stage('Build Docker Image') {
      steps {
        sh 'docker build -t $IMAGE_NAME:$IMAGE_TAG .'
      }
    }

    stage('Push Image to DockerHub') {
      steps {
        withCredentials([usernamePassword(
          credentialsId: 'dockerhub-creds',
          usernameVariable: 'DOCKER_USER',
          passwordVariable: 'DOCKER_PASS'
        )]) {
          sh '''
            echo "$DOCKER_PASS" | docker login -u "$DOCKER_USER" --password-stdin
            docker push $IMAGE_NAME:$IMAGE_TAG
          '''
        }
      }
    }

  }
}

