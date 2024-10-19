pipeline{
    agent any
    environment {
        DEPLOY_TO = 'Xyz'
    }
    stages{
        stage('DeployToDev'){
            steps{
                echo "Deploy to Dev"
            }
        }
        stage('DeployToTest'){
            steps{
                echo "Deploy to Test"
            }
        }
         stage('DeployToStage'){
            when{
                branch 'release/*'
            }
            steps{
                echo "Deploy to Stage"
            }
        }
         stage('DeployToProd'){
            when{
                //VX.X.X
                tag pattern: "v\\d{1,2}.\\d{1,2}\\.d{1,2}", comparator: "REGEXP"
            }
            steps{
                echo "Deploy to Production"
            }
        }
    }
}
