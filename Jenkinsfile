node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'Test-Sonar-Scanner';
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/Test-Sonar-Scanner"
    }
  }
}

