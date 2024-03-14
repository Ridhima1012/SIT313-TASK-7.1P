pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'RIDHIMA', url: 'https://github.com/Ridhima1012/my-app']])
                echo 'Building the code'
            }
        }
  
        stage('Unit and Integration Tests') {
            steps {
                echo 'Executing unit and integration tests: Successfully'
            }
            post {
                success {
                    mail to: 'ridhima1012c@gmail.com',
                        subject: 'Executing unit and integration tests: Successfully',
                        body: 'Both integration and unit tests passed. Check logs for more information.'
                        //attachLog: true
                }
                failure {
                    mail to: 'ridhima1012c@gmail.com',
                        subject: 'Executing unit and integration tests: Failed',
                        body: 'Both integration and unit tests have failed. Check logs for more information.'
                        //attachLog: true
                        
                }
                 
             }
        }
        

        stage('Code Analysis') {
            steps {
                echo 'Executing code analysis'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Performing security checks'
            }
            post {
                success {
                    mail to: 'ridhima1012c@gmail.com',
                        subject: 'Secuirty scan done: Successfully',
                        body: 'Security scans passed.Check logs for more information.'
                        //attachLog: true
                }
                failure {
                    mail to: 'ridhima1012c@gmail.com',
                        subject: 'Security Scans: Failed',
                        body: 'Security scans have failed. Check logs for more information. '
                        //attachLog: true
                        
                }
                 
             }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Executing integration tests on staging'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production...'
            }
        }
    }
}

    


