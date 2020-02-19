pipeline {
   agent any

   stages {
      stage('Build & SonarQube analysis') {
         steps {
            withSonarQubeEnv('My SonarQube Server') {
				sh 'mvn clean package sonar:sonar'
			}
         }
      }
   }
}
