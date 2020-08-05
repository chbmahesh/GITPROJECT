pipeline {
	agent any
		stages {
		stage('Check Out') {
			steps {
			    git 'https://github.com/chbmahesh/WebApplication.git'
				echo "Checking out code from Git repo."
			}
		}
		stage('Build') {
			steps {
				
				echo "Building Maven build."
			}
		}
		stage('Deploy') {
			steps {
				echo "Deploying into webapplication server."
			}
		}
		stage('Test') {       
			steps {
			echo "Running Selenium test scripts."
			}        
		}
		stage ('Email') {
			steps{
				
			mail bcc: '', body: '''Jenkins Pipeline status success !!!
 
			Thanks !!!''', cc: '', from: '', replyTo: '', subject: 'Jenkins Pipeline status', to: 'chbmaheshrao001@gmail.com'
			}
		}
	}
}
