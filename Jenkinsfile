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
                echo "Hello World!"
		input 'Feature good ?'
            }
            when {
                branch 'feat/*'
            }
        }
        stage('Build feature') {
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
                echo "Hello World!"
                input 'Release candidate ?'
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
