pipeline{

    agent any 
    stages{
        stage("Build"){
            steps{
                echo " Build the app"
            }
        }
        satage('Test'){
            steps{
               echo "testing the app"
            }
        }
        stage('DeployToDev'){
            steps{
                echo "Deploying to dev env"
            }
        }
        stage('DeployToProd'){
            steps{
                timeout (time: 300, unit: 'SECONDS'){
                input message: 'would you like to promote to prod ??', ok: 'yes', submitter: 'anu'
                }
                echo "Deploy to prod"
            }
        }
         
    }
}
