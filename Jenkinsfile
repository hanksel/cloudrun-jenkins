echo 'Se inicio el pipeline'



pipeline {
   agent any



stages {
    stage('Run gcloud') {
        steps {
		        sh "cat /etc/os-release"
		        sh "pwd"
				sh "ls"

                sh "gcloud --version"
				sh "gcloud auth list"
        }
    }
	  
	
    stage('Dockercheck') {
        steps {
		        sh "sudo apt-get update"
				
        }
    }
    
}
}

echo 'Fin del pipeline'