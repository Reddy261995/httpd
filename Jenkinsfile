pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                echo " build the application"
            }

        }
        stage('parallelstagescans'){
            parallel{
                stage ('sonar'){ 
                    steps{
                        echo "sonar stage execute"
                        sleep 20
                    }
                }
                stage ('Fortify'){ 
                    steps{
                        echo "sonar fortify execute"
                        sleep 20
                    }
                }
                stage ('prisma'){ 
                    steps{
                        echo "sonar prisma  execute"
                        sleep 20
                    }
                }
            }
        }
    }
}
