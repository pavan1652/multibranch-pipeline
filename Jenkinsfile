pipeline {
    agent any
    stages {
		stage('checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']],
				userRemoteConfigs: [[url: 'https://github.com/pavan1652/ansibletest.git']]])
            }
        }
        stage('Build') {
            steps {
                echo 'Building 123..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
				sh 'echo printnv'
                echo 'Deploying....'
            }
        }
    }
}