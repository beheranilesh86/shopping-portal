pipeline {
  agent any
  stages {
    stage('build-the-app') {
      steps {
        echo 'this is the build job'
        sh 'npm install'
      }
    }

    stage('test-the-app') {
      steps {
        echo 'this is the test job'
        sh 'npm test'
      }
    }

    stage('three') {
      steps {
        echo 'this is the package job'
        sh 'npm run package'
      }
    }

    stage('archive-the-artifacts') {
      steps {
        archiveArtifacts '**/distributiion/*.zip'
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