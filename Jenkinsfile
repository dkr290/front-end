pipeline{

    agent any


    tools{
        nodejs 'nodejs-4.8.6'
    }


    stages{
        stage('build'){
            steps{
                echo 'this is the compile job'
                sh 'npm install'

            }
        }
        stage('test'){
            steps{
                echo 'this is the test job'
                sh 'npm test'

            }
        }
        stage('package'){
            steps{
                echo 'this is the package job'
                sh 'npm run package'

            }
        }
    }

    post{
        always{

            archiveArtifacts artifacts: '**/distribution/*.zip'
        }

    }

}

