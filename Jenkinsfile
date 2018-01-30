node {
   def mvnHome
   stage('Clean') {
        deleteDir()
    }
    stage('Checkout') {
        checkout scm
    }
    stage('Build') {    
		def atlsa-mvn= tool 'atlsa-mvn'
           if (isUnix()) {
				sh "'${atlas-mvn}/bin/mvn' package"
			}
			else{
				bat "'${atlas-mvn}/bin/mvn' package"
		   }	
    }
}