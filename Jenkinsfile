pipeline{
  environment{
    DOCKERHUB_CREDENTIALS=credentials('dockerhub')
  }
  stages{
    stage('Build'){
      steps{sh 'docker build -t ahmedwahid/angular-image .'}
    }
     stage('login'){
      steps{sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'}
    }
    stage('Push'){
      steps{sh 'docker push ahmedwahid/angular-image'}
    }
  }

}
