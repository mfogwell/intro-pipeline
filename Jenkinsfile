pipeline {
  agent any
  stages {
    stage('Say Hello') {
      steps {
        echo "Hello ${params.Name}!"
        echo "${TEST_USER_USR}"
        echo "${TEST_USER_PSW}"
      }
    }
    stage('Deploy') {
      options {
        timeout(time: 30, unit: 'SECONDS')
      }
      input {
        message 'Should we continue?'
      }
      steps {
        echo 'Continuing with deployment'
      }
    }
  }
  environment {
    MY_NAME = 'Michelle'
    TEST_USER = credentials('test-user')
  }
  options {
    timeout(time: 15, unit: 'SECONDS')
  }
  parameters {
    string(name: 'Name', defaultValue: 'whoever you are', description: 'Who should I say hi to?')
  }
}