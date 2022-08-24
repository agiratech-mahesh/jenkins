pipeline {
    agent any
        stages {
            stage ('checkout') {
                steps {
                     checkout scm
                }
            }
            stage ('k8s') {
            steps {
            sh " minikube delete "
            sh " minikube start "
            }
            }
            stage ('minikube') {
                steps {
                sh "docker build -t maheshagiratech/k8s . "
                sh "docker push maheshagiratech/k8s "}}
            sh " kubectl create -f deployment.yml "
            sh " kubectl create -f service.yml "
            sh " minikube service snap-service --url "
            sh " kubectl describe pods "
            sh " kubectl get pods "
            sh " kubectl describe pods "
            sh " kubectl get pods,svc "
            sh " kubectl describe pods "
            sh " kubectl describe pods "
                sh " kubectl describe pods "
                sh " kubectl describe pods "
                sh " kubectl describe pods "
                sh " kubectl describe pods "
                sh " kubectl describe pods "
                sh " kubectl describe pods "
                sh " kubectl describe pods "
                sh " kubectl describe pods "
                sh " kubectl describe pods "
                sh " kubectl describe pods "
                sh " kubectl describe pods "
                sh " kubectl describe pods "
                sh " kubectl describe pods "
                sh " kubectl describe pods "
                sh " kubectl describe pods "
                sh " kubectl describe pods "
                sh " kubectl describe pods "
                sh " kubectl describe pods "
                sh " kubectl describe pods "
            }
            }
        }
}
            
