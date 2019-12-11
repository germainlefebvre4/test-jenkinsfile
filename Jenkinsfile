pipeline {
    agent {
        label "jenkins-agent"
    }
    stages {
        stage('Test') {
            steps {
                echo "Hello World!"
            }
            when {
	        anyOf {
                    branch 'feat/*'
		    branch 'hotfix/*'
		    branch 'develop'
		}
            }
        }
        stage('Build') {
            steps {
	        checkout scm
                echo "Hello World!"
            }
            when {
	        anyOf {
                    branch 'feat/*'
		    branch 'hotfix/*'
		    branch 'develop'
		}
            }
        }
        stage('Deploy Dev') {
            steps {
                echo "Hello World!"
            }
            when {
                branch 'feat/*'
            }
        }
        stage('Deploy Qual') {
            steps {
                echo "Hello World!"
            }
            when {
                branch 'develop'
            }
        }
        stage('Release candidate') {
            steps {
                input 'Release candidate ?'
            }
            when {
                branch 'develop'
            }
        }
        stage('Deploy Preprod') {
            steps {
                echo "Hello World!"
            }
            when {
                branch 'master'
            }
        }
        stage('Deploy Hotfix') {
            steps {
                echo "Hello World!"
            }
            when {
                branch 'hotfix/*'
            }
        }
        stage('Release stable') {
            steps {
                input 'Release candidate ?'
            }
            when {
                branch 'master'
            }
        }
        stage('Deploy production') {
            steps {
                echo "Hello World!"
            }
            when {
                branch 'master'
            }
        }
    }
}
