echo 'Se inicio el pipeline'



pipeline {
   agent any

stages {
    stage('Run gcloud') {

        steps {
				pwd()

				sh find /var -name gcloud

            withEnv(['GCLOUD_PATH=/var/jenkins_home/google-cloud-sdk/bin']) {
                sh '$GCLOUD_PATH/gcloud --version'
            }


         }
      }
   }
}

echo 'Fin del pipeline'