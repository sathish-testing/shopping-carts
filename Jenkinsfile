pipeline {
  agent any
  stages {
    stage('compile') {
      steps {
        echo 'this is the compile job'
        sh 'mvn compile'
      }
    }

    stage('test') {
      steps {
        echo 'this is the test job'
        sh 'mvn test'
      }
    }

    stage('package') {
      steps {
        echo 'this is the package job'
        sh 'mvn package -DskipTests'
        sleep 7
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
      echo 'this is my first pipeline...'
    }

  }
}

