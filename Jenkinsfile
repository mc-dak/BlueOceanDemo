pipeline {
  agent any
  stages {
    stage('checkoutGit') {
      steps {
        git(url: 'https://github.com/elestopadov/jenkins-example-app.git', branch: 'main')
      }
    }

    stage('build') {
      steps {
        echo 'this is build'
      }
    }

    stage('deploy') {
      parallel {
        stage('deploy1') {
          steps {
            sleep 50
            echo 'finished deploy1'
          }
        }

        stage('deploy2') {
          steps {
            sleep 30
            echo 'finished deploy-2'
          }
        }

      }
    }

    stage('test') {
      steps {
        echo 'testing'
      }
    }

  }
}