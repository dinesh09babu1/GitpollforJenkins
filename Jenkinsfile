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
          BRANCH_NAME == 'master'
        }
      }
      steps{
      echo "This is test stage"
      }
    }
  }
}
