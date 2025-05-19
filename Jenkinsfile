pipeline {
	agent any
	
	stages {
		stage("checout") {
			steps {
				git "repo-url"
			}
		}

		stage("build docker image") {
			steps {
				script {
					dockerImage = docker.build("jenkins-docker-basic:latest")
				}
			}
		}
		
		stage("run container") {
			steps {
				script {
					dockerImage.run()
				}
			}
		}
	}

}
