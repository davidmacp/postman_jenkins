pipeline {
  agent any

  stages {
    stage('API tests') {
      steps {
        sh "docker run -v `pwd`:/etc/newman -t postman/newman_ubuntu1404 --collection \"collection.json\" --environment=\"environment.json\""
      }
    }
  }
}
