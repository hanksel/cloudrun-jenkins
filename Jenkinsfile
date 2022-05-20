echo 'Se inicio el pipeline'



pipeline {
   agent any

stages {
    stage('Run gcloud') {

        steps {
				sh "pwd"

				sh "ls /var"

                sh "gcloud --version"


         }
      }
   }
}

echo 'Fin del pipeline'