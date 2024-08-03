node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'practice-site';
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/practice-site"
    }
  }
}

