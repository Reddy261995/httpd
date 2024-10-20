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
        always{
       // mail bcc: '', body: 'Build is success', cc: '', from: '', replyTo: '', subject: 'Jenkins status', to: 'reddykalamukuntla26@gmail.com'
          script{
              def subject = "Job status is:" ${currentBuild.currentResult}
              def body = "Build Number is: ${currentBuild.number}\n" + "status is: ${currentBuild.currentResult}\n" + "job URL: ${env.BUILD_URL}"
              mail{
                  to 'reddykalamukuntla26@gmail.com'
                  subject subject
                  body body
              }
            }
         }

    }
}
