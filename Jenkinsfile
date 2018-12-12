pipeline {
 agent any
 stages{
  stage('Checkout external proj') {
        steps {
            git branch: 'master',
                credentialsId: 'nmsrinivas',
                url: 'ssh://git@github.com:nmsrinivas/cicd-pipeline-gradle.git'

            sh "ls -lat"
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
