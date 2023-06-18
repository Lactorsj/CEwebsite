pipeline {
  agent any
  stages {
    stage('Build our website') {
      steps {
        chmod +x scripts/build.sh
        sh "scripts/build.sh"
      }
    }

    stage('Run unit tests') {
      steps {
        chmod +x scripts/unit_tests.sh
        sh "scripts/unit_tests.sh"
      }
    }

    stage('Deloy website') {
      steps {
        chmod +x scripts/deploy_website.sh
        sh "scripts/deploy_website.sh"
      }
    }
  }
}
