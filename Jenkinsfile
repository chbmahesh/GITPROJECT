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
			mail bcc: '', body: '''Jenkins job executed Successfully !!!!

			Thank you !!!''', cc: 'rajeshberi369@gmail.com;Vijaysurnila@gmail.con', from: '', replyTo: '', subject: 'Jenkins Build Staus', to: 'chbmaheshrao001@gmail.com;sharathagapes@gmail.com;rathodgopal98@gmail.com;manikanta.4b1@gmail.com;'
			}
		}
	}
}
