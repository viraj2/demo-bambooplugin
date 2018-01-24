node {
   def mvnHome
   stage('Preparation') { // for display purposes
      git 'https://github.com/viraj2/demo-bambooplugin.git'         
      mvnHome = tool 'Maven'
   }
   stage('Build') {
      // Run the maven build
      if (isUnix()) {
         sh "'${mvnHome}/bin/mvn' atlas-package"
      } else {
         bat(/"${mvnHome}\bin\mvn" atlas-package/)
      }
   }
   stage('Results') {
      junit '**/target/surefire-reports/TEST-*.xml'
      archive 'target/*.jar'
   }
}