pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git credentialsId: '<your-github-credentials>', url: '<your-github-repo-url>'
      }
    }
    stage('Deploy') {
      steps {
        bat "\"C:\\xampp\\xampp_stop.exe\""
        bat "xcopy /Y /S \"${WORKSPACE}\" \"C:\\xampp\\htdocs\\\""
        bat "\"C:\\xampp\\xampp_start.exe\""
      }
    }
  }
}
