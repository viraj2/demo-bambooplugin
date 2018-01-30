node {
   def atlas
   stage('Clean') {
        deleteDir()
    }
    stage('Checkout') {
        checkout scm
    }
    stage('Build') {    
			atlas= tool 'atlas-mvn'
           if (isUnix()) {
				sh "${atlas}/bin/atlas-package"
			}
			else{
				bat "${atlas}\bin\atlas-package"
		   }	
    }
}