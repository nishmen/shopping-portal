pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'this is to build the app'
        sh 'npm install'
      }
    }

    stage('test') {
      steps {
        echo 'this is to test the app'
        sh 'npm test'
      }
    }

    stage('package') {
      steps {
        echo 'this is to package the app'
        sh 'npm run package'
      }
    }

    stage('archive') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}