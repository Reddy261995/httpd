pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                echo "Building the applicaltion "
            }
        }
    }
    post{
        // only Run this, when the current popeline or stage has a sucess status
        success{
           echo "post =====> sucess is triggered"
        }
        //only runs when the current pipeline or stage is having a failure status
        failure{
           echo " post ====> failure got triggered" 
        }
        // This will run irrespective of failure or sucess.. meaning everytime
        always{
            // block
            echo " alway got triggerd"
        }
    }
}
