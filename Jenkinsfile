pipeline {
    agent { 
        label 'minikube'
    }
 
    stages {
 
        stage('git clone') {
            steps {
                sh 'rm -rvf Jenkinsfile_Minikube'
                sh 'git clone https://github.com/Deepak9829/Jenkinsfile_Minikube.git'
                sh 'pwd'
                sh 'ls -l Jenkinsfile_Minikube'
            }
        }
 
        stage('Helm Package Install') {
            steps {
                sh 'sudo /usr/local/bin/helm install kltestchart kltestchart/'
            }
        }
 
        stage('See Kubernetes Resources') {
            steps {
                sh 'sudo kubectl get all'
            }
        }
    }
}
