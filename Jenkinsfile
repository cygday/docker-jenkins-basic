pipeline {
	agent any
	
	stages {
		stage("checout") {
			steps {
				git branch: "main", url: "https://github.com/cygday/docker-jenkins-basic.git"
			}
		}

		stage("build docker image") {
			steps {
				script {
					sh "docker build -t jenkins-docker-basic:latest . ")
				}
			}
		}
		
		stage("run container") {
			steps {
				script {
					sh "docker run -d jenkins-docker-basic:latest"
				}
			}
		}
	}

}
