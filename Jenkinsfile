pipeline {
  agent any

    stages {
          stage('API tests') {
            steps {
              // sh "docker run -v /var/run/docker.sock:/var/run/docker.sock -v `pwd`:/etc/newman -t postman/newman_ubuntu1404 --collection \"collection.json\" --environment=\"environment.json\""
              sh "pwd"
              // sh "docker run -t postman/newman_ubuntu1404 collection \"https://www.getpostman.com/collections/d45b3b20f83cc5f532fa\""
              sh "docker run -v `pwd`:/etc/newman -t postman/newman_ubuntu1404 --collection \"collection.json\" --environment=\"environment.json\""
            }
      }
  }
}
