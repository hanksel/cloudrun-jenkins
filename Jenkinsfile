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
                        url: 'https://github.com/hanksel/cloudrun-jenkins',
                        branch : 'master'
                )
            }
    }
		
    
}
}

echo 'Fin del pipeline'