pipeline {
  agent any
  stages {
    stage('scm') {
      steps {
        git 'https://github.com/ananyachowhan/TomcatMavenApp'
      }
    }

    stage('Build') {
      steps {
        bat 'mvn -Dmaven.test.failure.ignore=true clean package'
      }
    }

  }
  tools {
    maven 'MAVEN3.9.9'
  }
  environment {
    name = 'staging'
  }
}