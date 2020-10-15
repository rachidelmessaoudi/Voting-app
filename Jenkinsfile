pipeline {
  agent {
    node {
      label 'master'
    }
  }
  stages {
    stage('Build result') {
      steps {
        sh 'docker build -t grini/result:latest ./result'
      }
    } 
    stage('Build vote') {
      steps {
        sh 'docker build -t grini/vote:latest ./vote'
      }
    }
    stage('Build worker') {
      steps {
        sh 'docker build -t grini/worker:latest ./worker'
      }
    }
    stage('Push result image') {
      steps {
          sh 'docker push grini/result:latest'
      }
    }
    stage('Push vote image') {
      steps {
          sh 'docker push grini/vote:latest'
      }
    }
    stage('Push worker image') {
      steps {
          sh 'docker push grini/worker:latest'
      }
    }
    stage('deployer containers') {
      steps {
          sh 'kubectl apply -f kube-deployment.yml'
      }
    }
  }
}
