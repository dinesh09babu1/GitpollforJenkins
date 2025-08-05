pipeline{
  agent any
  stages{
    environment{
      VERSION = '1'
    }
    stage("build"){
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
