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
              sh "docker run -t postman/newman_ubuntu1404 run \"https://www.getpostman.com/collections/8a0c9bc08f062d12dcda\""
            }
      }
  }
}
