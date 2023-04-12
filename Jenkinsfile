pipeline {
  agent {
    docker {
      image 'ubuntu'
    }
  }
  stages {
    stage('Build') {
      steps {
        // Add build steps here
      }
    }
    stage('Test') {
      steps {
        // Add test steps here
      }
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
