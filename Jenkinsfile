pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {
		    withCredentials([string(credentialsId: 'sonar-cloud-key', variable: 'SCK')]) {
			    sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=buggywebapp -Dsonar.organization=dbrink-devsecops -Dsonar.host.url=https://sonarcloud.io -Dsonar.login=${SCK}'
			}
        } 
  }
}
}
