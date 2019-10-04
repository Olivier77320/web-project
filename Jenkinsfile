pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				bat 'mvn clean package'
			}
			post {
				success {
					echo 'Now Archiving....'
					archiveArtufcats artifacts: '**/target/*.war'
				}
			}
		}	
	}
}