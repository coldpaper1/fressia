pipeline {
  agent any
  stages {


    stage('git clone!!!! ') {
      steps {
        sh '''
        sudo rm -rf /var/lib/jenkins/workspace/freesias/project1
        sudo git clone https://github.com/coldpaper1/project1.git
        cd project1

        sudo chmod 777 imagebuild.yaml
        '''
      }
    }
    stage('docker build & push & rolling-update ') {
      steps {
        sh '''

        sudo ansible-playbook imagebuild.yaml

        '''
      }
    }

  }
}
