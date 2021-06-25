pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo "Hello World!"
                sh "echo Hello from the shell"
                sh "hostname"
                sh "uptime"
                sh "wget https://dl.k8s.io/v1.20.6/kubernetes-client-linux-amd64.tar.gz; tar -zxvf kubernetes-client-linux-amd64.tar.gz; chmod +x kubernetes/client/bin/kubectl; mv kubernetes/client/bin/kubectl ."
                sh "./kubectl version"
                sh "./kubectl create ns test || true"
            }
        }
        stage('clean') {
            steps {
                echo "Delete namespace"
                sh "wget https://dl.k8s.io/v1.20.6/kubernetes-client-linux-amd64.tar.gz; tar -zxvf kubernetes-client-linux-amd64.tar.gz; chmod +x kubernetes/client/bin/kubectl; mv kubernetes/client/bin/kubectl ."
                sh "./kubectl version"
                sh "./kubectl delete namespace test || true"
            }
            when {
              pullRequest.merged
            }
        }
    }
}


