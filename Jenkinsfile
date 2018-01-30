node {
   def atlas-mvn
   stage('Clean') {
        deleteDir()
    }
    stage('Checkout') {
        checkout scm
    }
    stage('Build') {    
			atlsa-mvn= tool 'atlsa-mvn'
           if (isUnix()) {
				sh "'${atlas-mvn}/bin/mvn' package"
			}
			else{
				bat "'${atlas-mvn}/bin/mvn' package"
		   }	
    }
}