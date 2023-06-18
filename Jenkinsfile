pipeline {
  agent any
  stages {
    stage('Build our website') {
      steps {
        script {
          sh "chmod +x scripts/build.sh"
          sh "scripts/build.sh"
        }
      }
    }

    stage('Run unit tests') {
      steps {
        script {
          sh "chmod +x scripts/unit_tests.sh"
          sh "scripts/unit_tests.sh"
        }
      }
    }

    stage('Deploy website') {
      steps {
        script {
          sh "chmod +x scripts/deploy_website.sh"
          sh "scripts/deploy_website.sh"
        }
      }
    }
  }
}
