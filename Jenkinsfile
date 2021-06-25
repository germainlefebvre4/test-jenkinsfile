pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo "Hello World!"
                sh "echo Hello from the shell"
                sh "hostname"
                sh "uptime"
                sh "wget -q https://dl.k8s.io/v1.20.6/kubernetes-client-linux-amd64.tar.gz; tar -zxvf kubernetes-client-linux-amd64.tar.gz; chmod +x kubernetes/client/bin/kubectl; mv kubernetes/client/bin/kubectl ."
                sh "./kubectl version"
                sh "./kubectl create ns test || true"
                sh 'printenv'
            }
        }
        stage('clean') {
            steps {
                script {
                    if (env.pullRequest.isMerged) {
                        stage {
                            echo "Delete namespace"
                            sh "wget -q https://dl.k8s.io/v1.20.6/kubernetes-client-linux-amd64.tar.gz; tar -zxvf kubernetes-client-linux-amd64.tar.gz; chmod +x kubernetes/client/bin/kubectl; mv kubernetes/client/bin/kubectl ."
                            sh "./kubectl version"
                            sh "./kubectl delete namespace test || true"
                        }
                    }
                }
            }
//            when {
//                branch 'feat/test-merge'
//                // pullRequest.merged
//            }
        }
    }
}


