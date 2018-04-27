pipeline {
  agent any
  stages {
    stage('Say Hello') {
      steps {
        echo "Hello Michelle"
        echo 'Jenkins Test 6'
        echo "${TEST_USER_USR}"
        echo "${TEST_USER_PSW}"
      }
    }
     stage('Say Goodbye') {
      steps {
        echo "goodbye Michelle"
      }
    }

  }
  environment {
    MY_NAME = 'Mary'
    TEST_USER = credentials('test-user')
  }

}
