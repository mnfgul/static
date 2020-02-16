pipeline {
	agent any 
	stages {
		stage('Upload to AWS'){
			steps{
				sh 'echo "Upload to AWS S3 starting...."'
				withAWS(region: 'us-east-1', credentials:'aws-static') 
				{
					s3Upload(bucket:'mnfgl-udacity-jenkinspipeline', file:'index.html')
				}
				sh 'echo "Upload to AWS S3 finished!"'
			}
		}
	}
}