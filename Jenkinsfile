pipeline {
  agent any

  tools {
            maven "M3"
        }

  triggers {
        cron('H/10 * * * 4') //triggers every 10 minutes on Thursdays
    }
  
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
