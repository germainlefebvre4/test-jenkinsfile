pipeline {
    agent {
        label "jenkins-agent"
    }
    stages {
        stage('Build feature') {
            steps {
                echo "Hello World!"
            }
            when {
                branch 'feat/*'
            }
        }
        stage('Test feature') {
            steps {
	        checkout scm
		sh 'ls -l'
		sh 'ls -lR'
		input 'Feature good ?'
                echo "Hello World!"
            }
            when {
                branch 'feat/*'
            }
        }
        stage('Build develop') {
            steps {
                echo "Hello World!"
            }
            when {
                branch 'develop'
            }
        }
        stage('Release candidate') {
            when {
                branch 'master'
            }
            steps {
                input 'Release candidate ?'
                echo "Hello World!"
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
