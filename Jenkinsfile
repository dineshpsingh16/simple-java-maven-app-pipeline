pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args '-v /home/jenkins/.m2:/root/.m2'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean package'
      }
    }
    stage('Test') {
      steps {
        sh 'mvn  test'
      }
    }  
    stage('Deploy') {
      steps {
        sh 'whoami'
        sh 'pwd'
        sh 'ls -l ./jenkins/scripts/deliver.sh'
      }
    }    
  }
}
