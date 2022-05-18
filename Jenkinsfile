pipeline {
    agent any
 
    stages {
 
        stage('git clone') {
            steps {
                sh 'rm -rvf Jenkinsfile_Minikube'
                sh 'https://github.com/Deepak9829/Jenkinsfile_Minikube.git'
                sh 'pwd'
                sh 'ls -l Jenkinsfile_Minikube'
            }
        }
 
        stage('Helm Package Install') {
            steps {
                sh 'helm install KLChart KLChart/'
            }
        }
 
        stage('See Kubernetes Resources') {
            steps {
                sh 'kubectl get all'
            }
        }
    }
}
