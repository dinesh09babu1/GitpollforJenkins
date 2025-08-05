pipeline{
  agent any
  stages{
    stage("build"){
      steps{
      echo "This is build step"
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
