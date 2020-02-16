pipeline {
	agent any 
	stages {
		stage('Build'){
			steps{
				sh 'echo "Hello World! Welcome to Jenkins Pipelines"'
				sh ''' 
					echo "Multiple shell commands should work"
					ls -lah
				'''
			}
		}
	}
}