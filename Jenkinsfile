pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo "Hello World!"
                sh "echo Hello from the shell"
                sh "hostname"
                sh "uptime"
                sh "wget https://dl.k8s.io/v1.21.2/kubernetes-client-linux-amd64.tar.gz; tar -zxvf kubernetes-client-linux-amd64.tar.gz; chmod +x kubernetes/client/bin/kubectl; mv chmod +x kubernetes/client/bin/kubectl /usr/bin/"
                sh "kubectl version"
            }
        }
    }
}


