pipeline {
  agent any
  stages {
    stage('install') {
      steps {
        sh 'sudo apt Install Apache'
      }
    }

    stage('fetch code') {
      steps {
        git(url: 'https://github.com/Rosbata/batch-544-blueocean.git', branch: 'main', poll: true)
      }
    }

    stage('deploy code') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}