node {
   def mvnHome
   stage('Clean') {
        deleteDir()
    }
    stage('Checkout') {
        checkout scm
    }
    stage('Build') {    
           if (isUnix()) {
				sh "mvn compile"
				sh "mvn atlas-package"
			}
			else{
				bat "mvn compile"
				bat "mvn atlas-package"
		   }	
    }
}