pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean package'
      }
    }

    stage('Test and Generate Jacoco Report Stage') {
      steps {
        sh 'mvn test jacoco:report'
      }
    }

  }
}