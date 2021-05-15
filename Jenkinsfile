pipeline{
  agent any
  
  stages{
    stage('build'){
        steps{
            echo 'build stage'
        }
    }
        stage('test'){
          steps{
            echo 'test stage'
          }
    }
    stage('deploy'){
        when{
          expression{
            BRANCH_NAME == 'main'
            }
        }
        steps{
          echo 'deploy stage'
        }
    }
  }
}
