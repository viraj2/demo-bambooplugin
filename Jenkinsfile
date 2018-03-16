node {
   def atlas
   stage('Clean') {
        deleteDir()
    }
    stage('Checkout') {
        checkout scm
    }
    stage('Build') {    
	sh "atlas-package"
    }
}
