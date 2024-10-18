pipeline{
    agent any
    environment{
    DEPLOY_TO = 'XYZ'
    }
    stages{
        stage('deployToDev'){
            steps{
              echo "Deploy to dev"
            }
        }
        stage('DeploytoProd'){
            when{
                anyOf{
                branch 'production'
                environment name: 'DEPLOY_TO', value: 'production'
                }
            }
            steps{
                echo " deploy to prod"
            }
        }
    }

}
