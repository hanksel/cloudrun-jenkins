echo 'Se inicio el pipeline'



pipeline {
   agent any

node {
  git '…' // checks out Dockerfile & Makefile
  def myEnv = docker.build 'my-environment:snapshot'
  myEnv.inside {
    sh 'make test'
  }
}

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
	  
	
    stage('cloud run deploy') {
        steps {
		        sh "gcloud run deploy cloudrun-jenkins --region us-east4 --platform managed --port 3000 --allow-unauthenticated"
        }
    }
    
}
}

echo 'Fin del pipeline'