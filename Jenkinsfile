pipeline {
    agent any
    environment {
        MY_SECRET_PASSWORD = credentials('id') // Make sure 'id' is the correct ID of your credential
    }
    parameters {
        string(name: 'NAME', defaultValue: 'Reddy', description: 'Name of the person')
        text(name: 'PARA', defaultValue: '', description: 'Enter high-level fixes for the release')
        choice(name: 'ENV', choices: ['Dev', 'Test', 'Prod'], description: 'Which environment would you like')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Would you like to scan')
        password(name: 'SECRET', defaultValue: 'SECRET', description: 'Enter the password')
    }
    stages {
        stage('parametersExample') {
            steps {
                echo "Welcome ${params.NAME}"
                echo "Fixes done are ${params.PARA}"
                echo "Deploying to ${params.ENV}"
                echo "Are scans happening? ${params.TOGGLE}"
                echo "The password entered is ${params.SECRET}" // Assuming you meant params.SECRET here
                echo "The secret password is ${MY_SECRET_PASSWORD}" // Correcting the variable name typo
            }
        }
    }
}
