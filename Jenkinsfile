pipeline {
  agent {
        docker { image 'postman/newman_ubuntu1404' }
    }
    stages {
          stage('Test') {
              steps {
                  sh 'node --version'
              }
          }
          stage('API tests') {
            steps {
              // sh "docker run -v /var/run/docker.sock:/var/run/docker.sock -v `pwd`:/etc/newman -t postman/newman_ubuntu1404 --collection \"collection.json\" --environment=\"environment.json\""
              sh "docker run -t postman/newman_ubuntu1404 collection \"https://www.getpostman.com/collections/d45b3b20f83cc5f532fa\""
            }
      }
  }
}
