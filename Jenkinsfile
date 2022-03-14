pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            build 'Build'
          }
        }

        stage('Message') {
          steps {
            echo 'First Build Done'
          }
        }

      }
    }

    stage('Post Build') {
      parallel {
        stage('Post Build') {
          steps {
            archiveArtifacts '**'
          }
        }

        stage('Messgae') {
          steps {
            echo 'Archiving done'
          }
        }

      }
    }

  }
}