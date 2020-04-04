pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/pavansw/java-maven-jacoco.git', branch: 'master', poll: true)
      }
    }

  }
}