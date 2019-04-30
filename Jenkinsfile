pipeline {
	agent any
	
	stages {
		stage('Build') {
			steps {
				echo "Building en cours..."
				bat 'mvn cleanpackage'
			}
			post {
			    success {
			        echo 'Now Archiving...'
			        archiveArtifacts artifacts: '**/target/*.war'
			    }
			}
		}
	}
}