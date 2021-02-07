pipeline {
  agent none
  stages {
    stage('Non-Parallel Stage') {
      agent {
        label 'master'
      }
      steps {
        echo 'This stage will be executed first  :::blueocean_Editor'
      }
    }

    stage('Run Tests') {
      parallel {
        stage('Test On Windows') {
          agent {
            label 'windows_node'
          }
          steps {
            echo 'Task1 on Agent'
          }
        }

        stage('Test On Master') {
          agent {
            label 'master'
          }
          steps {
            echo 'Task1 on Master'
          }
        }

      }
    }

  }
}