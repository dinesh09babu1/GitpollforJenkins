pipeline{
  agent any
  environment{
      VERSION = '1'
    }
  stages{
    stage("build"){   
      steps{
      echo "This is build step ${VERSION}"
        echo "This is branch - ${env.BRANCH_NAME}"
      }
    }
    stage("test"){
      when{
        expression{
          env.BRANCH_NAME == 'master'
        }
      }
      steps{
      echo "This is test stage"
      }
    }
  }
}
