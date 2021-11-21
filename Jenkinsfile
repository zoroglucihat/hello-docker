pipeline {



 

  stages {

    stage('Checkout Source') {
      steps {
        git 'https://github.com/zorolos/hello-docker.git'
      }
    }



    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "hellodocker.yaml", kubeconfigId: "mykubeconfig")
        }
      }
    }

  }

}
