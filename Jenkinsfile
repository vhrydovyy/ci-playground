pipeline {
  agent any
  stages {
    stage('Pull latest changes') {
      steps {
        git(url: 'https://github.com/essence-tech/olive3', branch: 'OTD-0000-replace-flake8-with-prospector', credentialsId: 'github')
        dir(path: './behave') {
          sh '''pip install -r requirements.txt

'''
        }

      }
    }

  }
}