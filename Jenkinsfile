pipeline{
    agent any
    environment{
        MY_SCRET_PASSWORD = credentials(id)
    }
    parameters{
        string(name: 'NAME', defaultValue:'Reddy', description: 'Name of the person')
        text(name:'PARA',defaultValue: '', description: 'Enter hihlevel fixes for the release')
        choice(name:'ENV', choices:['Dev','Test','Prod'], description: 'which env would like')
        booleanParam(name:'TOOGLE', defaultValue: true, description:'would yo like to scan')
        password(name:'SECRET',defaultValue:'SECRET', description:'Enter the password')
    }
    stages{
        stage('parametersExample'){
            steps{
                echo " wellcome ${params.NAME}"
                echo " Fixes done are ${params.PARA}"
                echo " Deploying to ${params.ENV}"
                echo " are scan heppening ${params.TOOGLE}"
                echo " The password entered is ${MY_SCRET_PASSWORD_PSW}"
            }
        }
    }
}
