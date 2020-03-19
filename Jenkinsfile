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
				checkout([$class: 'GitSCM', branches: [[name: BRANCH_NAME]],
				userRemoteConfigs: [[url: 'https://github.com/pavan1652/ansibletest.git']]])
			}
        }
        stage('Build') {
            steps {
                echo 'Building 123..'
				echo 'checking auto trigger'
				echo 'adding new line'
				echo 'adding new line2'
				echo 'adding new line3'
				echo 'adding new line4'
				echo 'adding new line5'
				echo 'adding new line6'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
				script {
					if (env.BRANCH_NAME == 'develop') {
						echo 'in develop branch'
					} else {
						echo 'Pulling...' + env.BRANCH_NAME
						echo 'Pulling...' + env.DISABLE_AUTH
						echo 'Pulling...' + env.DB_ENGINE
						echo 'Deploying....'
					}
				}
            }
        }
    }
}