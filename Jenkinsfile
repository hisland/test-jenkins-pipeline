pipeline {
  agent any
  stages{
    stage('init'){
      steps{
          sh '''
          node --version
          npm config set registry https://registry.npmmirror.com
          npm i -d
          '''
      }
    }
    stage('build'){
      steps{
          sh '''
          npm run build-only
          '''
      }
    }
    stage('archive'){
      steps{
          archiveArtifacts artifacts: 'dist/**', onlyIfSuccessful: true,fingerprint:false
      }
    }
  }
}
