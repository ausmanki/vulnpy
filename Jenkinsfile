node {
    def app
    stage('Clone repository') {
      

        checkout scm
    }
   stage('SonarQube') {
    
    def scannerHome = tool 'SonarScanner 4.0';
    withSonarQubeEnv('My SonarQube Server') { // If you have configured more than one global server connection, you can specify its name
    bat "${scannerHome}/bin/sonar-scanner  -Dsonar.sources=. -Dsonar.password=Sonar123 -Dsonar.login=admin -Dsonar.projectKey=demo"     
        }
    }
}
