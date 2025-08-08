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
          env.BRANCH_NAME == null // BRANCH NAME is valid only for multi branch pipeline. NULL for normal pipeline job
        }
      }
      steps{
      echo "This is test stage"
      }
    }
  }
}
