pipeline {
  agent {
    docker {
      image 'nginx'
    }

  }
  stages {
    stage('Build') {
      steps {
        echo 'Build stage'
      }
    }

    stage('Test') {
      parallel {
        stage('TC1') {
          steps {
            sh 'echo "Test case1 succeed"'
          }
        }

        stage('TC2') {
          steps {
            sh 'echo "Test case1 succeed"'
          }
        }

      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy') {
          steps {
            echo 'Deploy stage'
          }
        }

        stage('Post Deploy') {
          steps {
            sh 'echo "Deploy succeed"'
          }
        }

      }
    }

  }
}
