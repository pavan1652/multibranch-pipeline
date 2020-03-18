pipeline {
    agent any
	environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE    = 'sqlite'
    }

    stages {
		stage('checkout') {
            /*steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']],
				userRemoteConfigs: [[url: 'https://github.com/pavan1652/ansibletest.git']]])
            }*/
			echo ""
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
				sh 'printenv'
                echo 'Deploying....'
            }
        }
    }
}