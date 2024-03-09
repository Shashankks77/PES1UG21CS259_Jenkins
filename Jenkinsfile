pipeline {
  agent any
  stages{
     stage('Build') {
            steps {
                build 'PES1UG21CS259-1'
                sh 'g++ hello1.cpp -o output'
              }
          }
      stage('Test') {
          steps {
                 sh './output'
            }
        }
      stage('Deploy') {
          steps {
              echo 'deploy'
            }
        }
    }
    post{
        failure{
            error 'Pipeline failed'

        }
    }
}
