#!groovy
@Library('jenkins-pipeline-lib') _

pipeline
{
  agent any
  triggers
  {
    //At 04:00 on every day-of-week from Monday through Friday.
    pollSCM('H 4 * * 1-5')
  }
  stages
  {
    stage('Build')
    {
      steps
      {
        sh 'mvn install'
      }
    }
    stage('Archive')
    {
      steps
      {
        archiveArtifacts './target/*.hpi'
      }
      post
      {
        failure
        {
          sendNotifications 'ARCHIVE_ERROR'
        }
      }
    }
  }
  post
  {
    always
    {
      // Report Status
      sendNotifications(currentBuild.result,currentBuild.changeSets)
      gitTagCleanup "${BUILD_NUMBER}"

      junit 'target/*Test.xml'
    }
    success
    {
      gitTagSuccess "${BUILD_NUMBER}"
    }
  }
}
