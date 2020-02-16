pipeline {
	agent any 
	stages {
		stage('Upload to AWS'){
			steps{
				withAWS(region: 'us-east-1', credentials:'aws-static') 
				{
					sh 'echo "Upload to AWS S3 starting...."'
					s3Upload(bucket:'mnfgl-udacity-jenkinspipeline', file:'index.html')
					sh 'echo "Upload to AWS S3 finished!"'
				}
			}
		}
	}
}