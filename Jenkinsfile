pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'compile'
        sh 'mvn compile'
      }
    }

    stage('test') {
      steps {
        echo 'test'
        sh 'mvn clean test'
      }
    }

    stage('package') {
      steps {
        echo 'package'
        sh 'mvn package -DskipTests'
      }
    }

    stage('') {
      steps {
        archiveArtifacts 'target/*.war'
      }
    }

  }
  tools {
    maven 'Maven 3.6.3'
  }
  post {
    always {
      echo 'This pipeline is completed..'
    }

  }
}