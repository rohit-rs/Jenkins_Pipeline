pipeline {
  agent any
  stages {
	stage('fetch') {
      steps {
        git 'https://github.com/rohit-rs/Jenkins_Pipeline.git'
        bat label: '', script: 'Fetch.bat'
      }
    }
    stage('build') {
      steps {
        bat label: '', script: 'Build.bat'
      }
    }
    stage('test') {
      steps {
        bat label: '', script: 'Test.bat'
      }
	}
	stage('deploy') {
        steps {
          echo "Deployment Successful"
        }
      }
    }

    post {
      always {
        echo "This will run always"
      }

      success {
        echo "This will run only if successful"
      }

      failure {
        echo "This will run only if failure"
      }

      unstable {
        echo "This will run only if run was marked unstable"
      }

      changed {
        echo "This will run only if the state of pipeline has changed"
      }

    }

  }
