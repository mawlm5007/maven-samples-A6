pipeline {
  agent any
  tools {
    maven 'DHT_MVN'
    jdk 'DHT_SENSE'
  }
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/mawlm5007/maven-samples-A6', branch: 'master')
      }
    }

    stage('run') {
      steps {
        sh '''mvn clean
mvn test
mvn verify'''
      }
    }

  }
}