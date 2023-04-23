pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git credentialsId: 'DeyushK', url: 'https://github.com/DeyushK/html/'
      }
    }
    stage('Deploy') {
      steps {
        bat "\"E:\\xampp\\xampp_stop.exe\""
        bat "xcopy /Y /S \"${WORKSPACE}\" \"E:\\xampp\\htdocs\\\""
        bat "\"E:\\xampp\\xampp_start.exe\""
      }
    }
  }
}
