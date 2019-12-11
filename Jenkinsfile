pipeline {
    agent any
    stages {
        stage('Feat build') {
            steps {
                echo "Hello World!"
            }
            when {
                branch 'feat/*'
            }
        }
        stage('Develop build') {
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
            input {
                message 'Release candidate ?'
	    }
            steps {
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
        stage('Hotfix build') {
            steps {
                echo "Hello World!"
            }
            when {
                branch 'hotfix/*'
            }
        }
        stage('Release stable') {
            input {
                message 'Release candidate ?'
	    }
            steps {
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
