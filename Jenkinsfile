pipeline {
  agent any
  stages {
    stage('Say Hello') {
      agent any
      steps {
        echo "Hello ${params.name}!"
        echo 'Jenkins Test 6'
        echo "${TEST_USER_USR}"
        echo "${TEST_USER_PSW}"
      }
    }
    stage('Say Goodbye') {
      agent any
      steps {
        echo 'goodbye Michelle'
      }
    }
  }
  environment {
    MY_NAME = 'Mary'
    TEST_USER = credentials('test-user')
  }
  parameters {
    string(name: 'Name', defaultValue: 'why', description: 'Who should I say hi to?')
  }
}