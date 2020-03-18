pipeline {
    agent any
	environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE    = 'sqlite'
    }

    stages {
		stage('checkout') {
			echo "checkout"
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