pipeline {
  agent any
  stages {
    stage('compile') {
      steps {
        echo 'this is the first job'
        sh 'mvn compile'
      }
    }

    stage('test') {
      steps {
        echo 'this is the second job'
        sh 'mvn test'
      }
    }

    stage('package') {
      steps {
        echo 'this is the third job'
        sh 'mvn package -DskiptTests'
      }
    }

    stage('archive') {
      steps {
        archiveArtifacts '**/target/*.jar'
      }
    }

  }
  tools {
    maven 'maven'
  }
  post {
    always {
      echo 'this is my first pipeline has completed...'
    }

  }
}