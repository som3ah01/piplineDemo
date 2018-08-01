pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                 echo 'Now Building...'
            }
            
        }
        stage('Deploy to staging'){
            steps{
                echo 'Now Deploying...'

            }
        }
        stage('Deploy to production'){
            steps{
                timeout(time:5 , unit:'DAYS'){
                    input message: 'QA Aprove To Production Deployment?'
                }
                echo 'Now Production...'
            }
        }
    }
}