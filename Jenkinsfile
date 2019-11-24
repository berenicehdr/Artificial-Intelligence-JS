pipeline {
  agent any
  stages {
    stage('snyk dependency scan') {
      tools {
        snyk 'SynkSecurity'
      }	
      steps {
        snykSecurity(
        projectName: 'prueba_vulnerabilidades', severity: 'high', snykInstallation: 'SynkSecurity', snykTokenId: 'my-projectjs-snyk-api-token'
      	
        )
        sh 'npm audit'		
      }
     }
  }
}
