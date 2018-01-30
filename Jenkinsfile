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
				sh "atlas-mvn package"
			}
			else{
				bat "mvn compile"
				bat "atlas-mvn package"
		   }	
    }
}