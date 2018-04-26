pipeline {
  agent any

  stages {
    stage('API tests') {
      steps {
        sh "sudo docker run -v /var/run/docker.sock:/var/run/docker.sock -v `pwd`:/etc/newman -t postman/newman_ubuntu1404 --collection \"collection.json\" --environment=\"environment.json\""
      }
    }
  }
}
