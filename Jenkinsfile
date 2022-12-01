pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/devopsdeepdive/blueocean-repo.git', branch: 'master', credentialsId: 'github_cred')
      }
    }

    stage('Build') {
      steps {
        sh '//mvn compile'
      }
    }

    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }

    stage('Package') {
      steps {
        warnError(message: 'successful') {
          sh 'pwd'
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deployed succesfully'
      }
    }

  }
}