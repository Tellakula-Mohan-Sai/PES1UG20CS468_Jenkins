pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        sh 'g++ hello.cpp'
        build job: "PES1UG20CS468-1"
        echo 'build stage successful'
      }
    }
    stage('Test'){
      steps{
        sh './a.out'
        echo 'Test stage successful'
      }
    }
    stage('Deploy'){
      steps{
        echo 'deployed'
      }
    }
  }
  post{
    failure{
      echo 'Pipeline failed'
    }
  }
}
