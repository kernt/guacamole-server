pipeline {
  agent { label 'public' }
  options {
    timeout(time: 60, unit: 'MINUTES')
  }
    agent {
        docker {
            image 'debian:latest'
            args '-v $HOME/.m2:/root/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B'
            }
        }
    }
}
