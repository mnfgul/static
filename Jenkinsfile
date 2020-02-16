pipeline {
	agent any 
	stages {
		stage('Upload to AWS'){
			steps{
				sh 'echo "Upload to AWS S3 starting...."'
				withAWS(region: 'us-east-1', credentials:'IDofAwsCredentials') 
				{
					s3Upload(bucket:'mnfgl-udacity-jenkinspipeline')
				}
				sh 'echo "Upload to AWS S3 finished!"'
			}
		}
	}
}