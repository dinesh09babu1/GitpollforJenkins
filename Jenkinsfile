pipeline{
  agent any
  environment{
      VERSION = '1'
    SERVER_CREDENTIALS = credentials('dineshusername')
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
        echo "this is username=${SERVER_CREDENTIALS}"
        //withCredentials([
          //usernamePassword(credentials: 'server-credentials', usernameVariable: USER, passwordVariable: PASSWORD)
        //])
        //{
          //sh "some commands ${USER} ${PASSWORD}"
        //}
      }
    }
  }
}
