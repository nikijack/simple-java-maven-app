pipeline {
    agent any

    stages {
      stage('Checkout') {
        steps {
          git 'https://github.com/nikijack/simple-java-maven-app.git'
        }
      }
      stage('Maven Build') {
          steps {
              sh 'mvn clean install -Dmaven.repo.local=http://localhost:8081/repository/assign-maven-proxy/'
          }
      }
    }
}
