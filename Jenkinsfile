pipeline {
  agent any
  stages {
    stage('compile') {
      steps {
        echo 'this is the compile job'
        sh 'mvn compile'
        sleep 4
      }
    }

    stage('test') {
      steps {
        echo 'this is the test job'
        sh 'mvn test'
        sleep 9
      }
    }

    stage('package') {
      steps {
        echo 'this is the package job'
        sh 'mvn package -DskipTests'
        sleep 7
      }
    }

    stage('') {
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
      echo 'Hey this is my second development work related to shopping-carts|Pipeline has completed...'
    }

  }
}