pipeline {
    agent any
        stages {
            stage ('checkout') {
                steps {
                     checkout scm
                }
            }
            stage ('build') {
                steps {
                sh "docker build -t maheshagiratech/k8s . "
                sh "docker push maheshagiratech/k8s "
                }
                 }
            stage ('k8s') {
            steps {
            sh " minikube delete "
            sh " minikube start "
            sh " kubectl create -f deployment.yml "
            sh " kubectl create -f service.yml "
            sh " minikube service snap-service --url "
            }
            }
        }
}
            
