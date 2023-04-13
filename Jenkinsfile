pipeline {
  agent {
    docker {
      image 'ubuntu'
    }
  }
  stages {
    stage('Build') {
      steps {
        sh "echo BUILD"
      }
    }
    stage('Test') {
      steps {
        sh "echo TEST"
      }
    }
  }
  post {
    always {
      docker.image('ubuntu').withRun('-rm') {
        // Clean up the container after the build
      }
    }
  }
}
