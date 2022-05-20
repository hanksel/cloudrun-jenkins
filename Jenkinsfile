echo 'Se inicio el pipeline'



pipeline {
   agent any



stages {
    stage('Run gcloud') {
        steps {
				sh "ls /var"

                sh "gcloud --version"
				sh "gcloud auth list"
        }
    }
	  
	stage('Git checkout') {
            steps{
			    sh "git --version"
				sh "git clone 'https://github.com/hanksel/cloudrun-jenkins'"
				sh "ls"
            }
    }
    stage('Dockercheck') {
        steps {
				sh "Docker version"
        }
    }
    
}
}

echo 'Fin del pipeline'