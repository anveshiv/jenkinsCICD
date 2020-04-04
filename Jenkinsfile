pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/pavansw/java-maven-jacoco.git', branch: 'master', poll: true)
      }
    }

    stage('test') {
      steps {
        sh 'mvn test'
      }
    }

    stage('Publish') {
      steps {
        jacoco(buildOverBuild: true, runAlways: true)
      }
    }

  }
}