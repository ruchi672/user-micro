node {
    
   stage('GIT CheckOut') {
    git 'https://github.com/Cape-mindtree/ordering-micro.git'
  }
  
  stage('Create deployment') {
    sh label: '', script: 'microk8s.kubectl create -f src/main/scripts/deployment-todo.yml'
  }
   stage('Create service') {
    sh label: '', script: 'microk8s.kubectl create -f src/main/scripts/service-todo.yml'
  }
   stage('Create ingress') {
    sh label: '', script: 'microk8s.kubectl create -f src/main/scripts/ingress.yml'
  }
   stage('Deploy to cluster') {
    sh label: '', script: 'kubectl get pods'
  }
}
