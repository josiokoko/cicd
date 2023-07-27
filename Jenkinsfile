pipeline {
	agent any

	environment {
		DOCKERHUB_CREDENTIALS=credentials('josiokoko')
	}

	stages {

		stage("Git Checkout") {
			steps {
				git branch: 'main', url: 'https://github.com/josiokoko/cicd.git'
			}
		}

		stage("Docker Build") {
			steps{
				sh "docker build -t josiokoko/timeserver ."
			}
		}

		stage("Authenticate") {
			steps{
				sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
				echo "Login complete..."
			}
		}


		stage("Push to Registry") {
			steps{
				sh "echo pushing..."
			}
		}

		stage("Cleanup") {
			steps{
				sh "echo cleanup..."
			}
		}


	}
}