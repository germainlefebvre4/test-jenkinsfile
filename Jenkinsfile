pipeline {
    agent {
        label "jenkins-agent"
    }
    stages {
        stage('Build feature') {
            steps {
	        checkout scm
                echo "Hello World!"
            }
            when {
	        anyOf {
                    branch 'feat/*'
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
        stage('Build Qual') {
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
                echo "Hello World!"
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
        stage('Build hotfix') {
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
                echo "Hello World!"
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
