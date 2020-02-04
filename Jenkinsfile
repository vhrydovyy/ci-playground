pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        git(url: 'https://github.com/essence-tech/olive3', branch: 'OTD-0000-replace-flake8-with-prospector', credentialsId: '1a505a7f-56cd-4cca-90ed-5cde12561213')
      }
    }

  }
}