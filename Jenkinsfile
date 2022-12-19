////scripted
// node {
// 	echo "Build"
// 	echo "Test"
// 	echo "Integration Test"
// 	echo "Deployment Test"
// }

////Declarative

pipeline {
	agent { docker { image 'node:16.16.0' } }
	stages {
		stage('Build') {
			steps {
				sh 'node --version'
				echo "Build"
			}
		}
		stage('Test') {
			steps {
				echo "Test"
			}
		}
		stage('Integration Test') {
			steps {
				echo "Integration Test"
			}
		}
	}

	post {
		always {
			echo "Im awesome. I run always"
		}
		success {
			echo "I run when you are successful"
		}
		failure {
			echo "I run when you fail"
		}
	}
}
