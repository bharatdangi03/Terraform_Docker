pipeline {
	 agent { 
	    any {
		   filename 'Dockerfile'
		   reuseNode false
		   //args "--TAG tmp --AWS_ACCESS_KEY_ID=test1 --AWS_SECRET_ACCESS_KEY=test2"
		   additionalBuildArgs "--build-arg 'TAG=tmp' --build-arg 'AWS_ACCESS_KEY_ID=${env.AWS_ACCESS_KEY_ID}' --build-arg 'AWS_SECRET_ACCESS_KEY=${env.AWS_SECRET_ACCESS_KEY}'"
        }		
	}
	 
	 stages {
		 stage('checkout') {
			 steps {
			  git([url: 'https://github.com/bharatdangi03/Terraform_Docker.git', branch: 'master'])
			 
			 }
		 }
	}
}
