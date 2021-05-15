def groovy_script

pipeline{
  agent any
  
  stages{
    stage('init'){
        steps{
          script{
              groovy_script = load "script.groovy"
            }
        }
    }
    stage('build'){
        steps{
          script{
              groovy_script.build()
          }
        }
    }
    stage('test'){
          steps{
            script{
                groovy_script.test()
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
                groovy_script.deploy()
            }
          }
    }
  }
}
