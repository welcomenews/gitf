pipeline {
  agent any
  stages {
  stage('Git clone') {
      steps {
        script {
          sh 'cd /home/sergey/jen/'
          checkout([$class: 'GitSCM', branches: [[name: '*/main']],
          userRemoteConfigs: [[url: 'https://github.com/welcomenews/gitf.git']]])
          //sh 'git tag v0.1'
          
          sh 'cp /var/lib/jenkins/workspace/create_jenkinsfile_main/Jenkinsfile /home/sergey/jen/'
          sh 'ls -l /home/sergey/jen/'
        }
      }
    }
    stage('New branch') {
      steps {
        sh 'git fetch --all'
        //sh 'git checkout -b v0.2-rc1'
        sh 'git push -u origin main'
      }
    } 
  }
}
