pipeline{
  agent any
  
  stages{
    stage('build'){
        steps{
          echo 'build stage BRANCH_NAME'
        }
    }
        stage('test'){
          steps{
            echo 'test stage BRANCH_NAME'
          }
    }
    stage('deploy'){
        when{
          expression{
            BRANCH_NAME == 'master'
            }
        }
        steps{
          echo 'deploy stage'
        }
    }
  }
}
