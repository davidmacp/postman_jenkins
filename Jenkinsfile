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
      }
  }
//   stages {
//     stage('API tests') {
//       steps {
//         sh "docker run -v /var/run/docker.sock:/var/run/docker.sock -v `pwd`:/etc/newman -t postman/newman_ubuntu1404 --collection \"collection.json\" --environment=\"environment.json\""
//       }
//     }
//   }
// }
