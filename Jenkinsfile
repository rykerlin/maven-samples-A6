pipeline {
  agent any
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/rykerlin/maven-samples.git', branch: 'master')
      }
    }

    stage('clean') {
      steps {
        sh 'mvn clean'
      }
    }

    stage('install') {
      steps {
        sh 'mvn clean install'
      }
    }

    stage('test') {
      steps {
        sh 'mvn test'
      }
    }

    stage('verify') {
      steps {
        sh 'mvn verify'
      }
    }

    stage('after_clean') {
      steps {
        sh 'mvn clean'
      }
    }

  }
  tools {
    maven 'DHT_MVN'
    jdk 'Java8'
  }
}
