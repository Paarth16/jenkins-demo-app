pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        git 'https://github.com/YOUR_USERNAME/jenkins-demo-app.git'
      }
    }
    stage('Build Docker image') {
      steps {
        script {
          docker.build("jenkins-demo-app:${env.BUILD_NUMBER}")
        }
      }
    }
    stage('Tests') {
      steps {
        echo 'Tests would run here'
      }
    }
    stage('Deploy to Kubernetes') {
      steps {
        echo 'kubectl apply -f k8s-deployment.yaml'
      }
    }
  }
}
