pipeline {
  agent any
  stages {
    stage('Pull latest changes') {
      steps {
        git(url: 'https://github.com/essence-tech/olive3', branch: 'OTD-0000-replace-flake8-with-prospector', credentialsId: 'github')
      }
    }

    stage('Tests') {
      steps {
        sh 'pip3 install -r behave/requirements.txt'
        sh 'prospector --profile behave/prospector-profile.yaml --output-format=pylint:./tmp/lint.txt'
      }
    }

  }
}