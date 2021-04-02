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
        sh 'git checkout v0.2-rc1'
        //git url: "https://github.com/welcomenews/gitf.git",
        //credentialsId: 'welcomenews', passwordVariable: '470913827_Serg_',
        //branch: v0.2-rc
      }
    } 
  }
}
