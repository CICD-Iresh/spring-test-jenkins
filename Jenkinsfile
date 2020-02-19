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
   }
}
