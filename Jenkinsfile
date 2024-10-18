pipeline{
    agent any
    {
        environment{
            DEPLOY_TO = 'production'
        }
    }
    stages{
        stage("DeployToDev"){
            steps{
             echo "deploy to Dev"
            }    
        }
        stage("DeploytoProd"){
            when{
                allOf{
                    //10 conditons, then all the 10 conditons should be stisfied
                    branch = 'productin'
                    environment name: DEPLOY_TO, actual: 'poduction'
                }
            }
            steps{
                echo "deploy to production"
            }
          }
    }
}
