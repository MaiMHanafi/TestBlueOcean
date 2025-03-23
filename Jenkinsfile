pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build Completed'
      }
    }

    stage('Test Stages') {
      parallel {
        stage('Test1') {
          steps {
            echo 'Start Testing ..... Test 1'
          }
        }

        stage('Test2') {
          steps {
            echo 'Running Test2'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deployment started ..'
        input(message: 'Are you sure you want to deploy ?', ok: 'Yes.')
      }
    }

  }
}