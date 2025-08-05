pipeline{
  agent any
  stages{
    stage("build"){
       environment{
      VERSION = '1'
    }
      steps{
      echo "This is build step ${VERSION}"
      }
    }
    stage("test"){
      when{
        expression{
          env.BRANCH_NAME == 'dev'
        }
      }
      steps{
      echo "This is test stage"
      }
    }
  }
}
