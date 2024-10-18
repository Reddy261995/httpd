pipeline{
    agent any
    environment{
        DEPLOY_TO = 'production'
    }
    stages{
        stage("Deploye to dev"){
           steps{
            echo "Deploying Dev environment"
           }
        }
        stage("prodDeploy"){
            when{
                // Branch codition
                expression {BRANCH_NAME ==~/(production|stage)/}
            }
           steps{
            echo "Deploying to production"
           }
        }   
    }
}
