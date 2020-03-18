pipeline {
    agent any
	environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE    = 'sqlite'
    }

    stages {
		stage('checkout') {
			steps {
				echo "checkout"
				checkout([$class: 'GitSCM', branches: [[name: env.BRANCH_NAME]],
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
				echo 'Pulling...' + env.BRANCH_NAME
				echo 'Pulling...' + env.DISABLE_AUTH
				echo 'Pulling...' + env.DB_ENGINE
                echo 'Deploying....'
            }
        }
    }
}