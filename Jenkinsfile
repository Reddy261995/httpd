pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                echo "Testing mail post job"
            }
        }
    }
    post{
        success{
        mail bcc: '', body: 'Build is success', cc: '', from: '', replyTo: '', subject: 'Jenkins status', to: 'reddykalamukuntla26@gmail.com'
    }
    }
}
