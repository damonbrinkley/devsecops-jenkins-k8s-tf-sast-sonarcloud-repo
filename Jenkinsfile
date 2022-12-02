pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=devsecopsbuggywebapp -Dsonar.organization=devsecopsbuggywebapp -Dsonar.host.url=https://sonarcloud.io -Dsonar.login='
			}
        } 
  }
}
