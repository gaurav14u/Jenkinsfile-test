#!/usr/bin/env groovy

@Library('shared-jenkins-lib@main')
def groovy_script

pipeline{
  agent any
  
  stages{
    stage('build'){
        steps{
          script{
              script.build()
          }
        }
    }
    stage('test'){
          steps{
            script{
              script.test()
              }
          }
    }
    stage('deploy'){
        when{
          expression{
            BRANCH_NAME == 'main'
            }
        }
          steps{
            script{
              print BRANCH_NAME 
              print currentBuild.result
              print currentBuild              
              script.deploy()
            }              
          }
    }
  }
}
