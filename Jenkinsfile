pipeline {
	agent any
	
	stages {
		stage("checout") {
			steps {
				git "https://github.com/cygday/docker-jenkins-basic.git"
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
