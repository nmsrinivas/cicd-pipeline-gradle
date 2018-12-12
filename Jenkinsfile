pipeline {
 agent any
 stages{
  stage('Checkout') {
        steps {
           dir('cicd-pipeline-gradle')
                git credentialsId: 'GITHUB', url: 'ssh://git@github.com:nmsrinivas/cicd-pipeline-gradle.git'
        }
    }
  stage('Build') {
   steps {
   echo 'Running Build Automation'
   sh './gradlew build --no-daemon'
   archiveArtifacts artifacts: 'dist/sampleapp.zip'
   }
  }
 }
}
