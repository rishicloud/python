pipeline{
    agent{ label 'rishi12' }
    triggers{ cron '0 * * * *'}
    stages{
        stage( 'checkout' ){
            steps{
                git url: 'https://github.com/bravatjammu/python.git',
                    branch: 'master'

            }
        }
        stage('build'){
            steps{
                sh 'pip install -r requirements.txt'
                sh 'flake8'

            }
        }
    }
