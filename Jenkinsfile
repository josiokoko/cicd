pipeline {
	agent any

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
				sh "echo authenticating..."
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