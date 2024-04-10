pipeline {
  agent any
  stages{
    stage('stage 1'){
      steps{
          sh 'echo "123"'
          sh '''
          echo "god 1"
          echo "god 2"
          echo "god 3"
          node --version
          npm config set registry https://registry.npmmirror.com
          npm i -d
          npm run build-only
          echo "god 4"
          '''
      }
    }
    stage('state 2'){
      steps{
          sh 'echo "step 2"'
      }
    }
  }
}
