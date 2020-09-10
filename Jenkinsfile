pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build completed'
        retry(count: 3) {
          sh 'wwwwwww'
        }

      }
    }

    stage('Test stages') {
      parallel {
        stage('Test2') {
          steps {
            echo 'Running test2'
          }
        }

        stage('Test1') {
          steps {
            echo 'Running Test1'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        input(message: 'Are you to deploy?', ok: 'Yes, I am sure')
        echo 'deployment completed'
      }
    }

    stage('Notify for new build') {
      steps {
        echo 'New build completed successfully'
      }
    }

  }
}