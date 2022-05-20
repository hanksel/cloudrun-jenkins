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
	  
	
    stage('Dockercheck') {
        steps {
		        sh "sudo apt-get update"
				sh "sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin"
        }
    }
    
}
}

echo 'Fin del pipeline'