pipeline {
  agent any
  stages {
  stage('Git clone') {
      steps {
        script {
          sh 'cd /home/sergey/jen/'
          checkout([$class: 'GitSCM', branches: [[name: '*/master']],
          userRemoteConfigs: [[url: 'https://github.com/welcomenews/gitf.git']]])
          sh 'ls -l'
        }
      }
    }
  }
}
