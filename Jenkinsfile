pipeline {
	agent any 
	stages {
		
		stage('Lint HTML'){
			steps{
				sh 'echo "Lint checking for HTML with Tidy"'
				sh 'tidy -q -e *.html'
			}
		}

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