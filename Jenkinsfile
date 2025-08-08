pipeline{
  agent any
  environment{
      VERSION = '1'
      SECRET = credentials('dineshusername')
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
        echo "this is username=${SECRET}"
        withCredentials([
          usernamePassword(credentials: 'dineshusername',usernameVariable: USER, passwordVariable: PASSWORD)
        ]){
          //echo "some commandsd ${USER}"
        }
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
