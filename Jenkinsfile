pipeline {
  agent any
  stages {
    stage('snyk dependency scan') {
      tools {
        snyk 'SynkSecurity'
      }	
      steps {
        snykSecurity(
        projectName: 'prueba_vulnerabilidades', severity: 'medium', snykInstallation: 'SynkSecurity', snykTokenId: 'my-projectjs-snyk-api-token'


	  sh '''
         snyk test
              ‘’’
        )		
      }
    }
  }
}
