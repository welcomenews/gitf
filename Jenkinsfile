pipeline {
  agent any
  stages {
  stage('Git clone') {
      steps {
        script {
          sh 'cd /home/sergey/jen/'
          sh 'git clone https://github.com/welcomenews/gitf.git'
          sh 'ls -l'
        }
      }
    }
  }
}
