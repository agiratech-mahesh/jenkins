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
                sh " chmod 777 /var/run/docker.sock "
                sh "sudo docker build -t maheshagiratech/k8s . "
                sh "sudo docker push maheshagiratech/k8s "
                }
                 }
            stage ('k8s') {
            steps {
            sh " minikube start "
            sh " kubectl create -f deployment.yml "
            sh " kubectl create -f service.yml "
            sh " minikube service snap-service --url "
            sh " minikube dashboard "
            }
            }
        }
}
            
