pipeline {
   agent any

   stages {
      stage('Build & SonarQube analysis') {
         steps {
            withSonarQubeEnv('TestInstance') {
				sh 'mvn clean package sonar:sonar'
			}
         }
      }
      stage("Quality Gate") {
	     steps {
		    timeout(time: 1, unit: 'HOURS') {
			   waitForQualityGate abortPipeline: true
			}
		 }
	  }
   }
}
