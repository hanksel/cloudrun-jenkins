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
	  
	stage('Git checkout') {
            steps{
			    sh "rm -r cloudrun-jenkins"
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