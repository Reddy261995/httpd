pipeline{
    agent any
    environment{
        DEPLOY_TO = 'production'
    }
    stages{
        stage("prodDeploy"){
            when{
                not{
                    equals expected: 'prod', actual: "${DEPLOY_TO}"
                }
            }
            steps{
                echo "deploy to production"
            }
        }
    }
}
