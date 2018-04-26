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
  }
  parameters {
    string(name: 'Name', defaultValue: 'whoever you are', description: 'Who should I say hi to?')
  }
}