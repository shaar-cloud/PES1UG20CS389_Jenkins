pipeline{
  agent any
  stages {
    stage('Build'){
      steps{
        sh 'g++ PES1UG20CS389.cpp'
        build job : 'PES1UG20CS389-1'
        echo 'built'
      }
    }
    stage('Test'){
      steps{
        sh './a.out'
        echo 'Tested'
      }
    }
  }
  post{
    failure{
      echo 'Failed'
    }
  }
}
