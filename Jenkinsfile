pipeline {

  agent any

  stages {

    stage('My Build stage 01') {
      steps {
        echo "failure" >> /tmp/demo/stage_01.txt
      }
    }

    stage('My Build stage 02') {
      steps {
        sh """
          echo "failure" >> /tmp/demo/stage_02_a.txt
        """
        echo "failure" >> /tmp/demo/stage_02_b.txt
      }
    }
   
  }

  post {
    always {
        echo "always" >> /tmp/demo/post_always.txt
    }

    success {
        echo "success" >> /tmp/demo/post_success.txt
    }

    failure {
        echo "failure" >> /tmp/demo/post_failure.txt
    }
  }



}
