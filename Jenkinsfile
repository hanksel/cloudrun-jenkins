echo 'Se inicio el pipeline'



pipeline {
   agent any



stages {
    stage('Run gcloud') {
        steps {
				sh "pwd"

				sh "ls /var"

                sh "gcloud --version"
				sh "gcloud auth list"
        }
    }
	  
	stage('Git checkout') {
            steps{
                git (
                        credentialsId: '<JENKINS_CREDENTIALS_ID>',
                        url: '<GIT_URL>',
                        branch : 'develop'
                )
            }
    }
		
    
}
}

echo 'Fin del pipeline'