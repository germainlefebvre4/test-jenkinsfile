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
            input {
                message 'Release candidate ?'
		ok 'Yes'
	    }
            steps {
                echo "Hello World!"
            }
            when {
                branch 'master'
            }
        }
        stage('Preprod deploy') {
            steps {
                echo "Hello World!"
            }
            when {
                branch 'master'
            }
        }
        stage('Release stable') {
            input {
                message 'Release candidate ?'
		ok 'Yes'
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
        stage('Hotfix build') {
            steps {
                echo "Hello World!"
            }
            when {
                branch 'hotfix/*'
            }
        }
    }
}
