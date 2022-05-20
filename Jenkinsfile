echo 'Se inicio el pipeline'



pipeline {
   agent any



stages {
    stage('Run gcloud') {
        steps {
		        sh "pwd"
				sh "ls"

                sh "gcloud --version"
				sh "gcloud auth list"
        }
    }
	  
	
    stage('Dockercheck') {
        steps {
		        build(image[, args])
				
        }
    }
    
}
}

echo 'Fin del pipeline'