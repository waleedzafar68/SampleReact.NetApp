pipeline {
    agent any
    tools {
        nodejs 'nodejs'
	
    }
    parameters {
	    //choice(name:'VERSION', choices:['1.0', '1.1', '1.2'], description:'Choose the version of the project')

        booleanParam(name :'executeTests', description:'Execute the tests', defaultValue:false)
    }

    stages {
        stage('Install Dependencies and Server setup') {
            steps {
                sh '''' wget https://packages.microsoft.com/config/ubuntu/22.10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
                        sudo dpkg -i packages-microsoft-prod.deb
                        sh rm packages-microsoft-prod.deb  
                        sudo apt update && \
                        sudo apt install -y dotnet-sdk-6.0
                        sudo apt-get update && \
                        sudo apt-get install -y aspnetcore-runtime-7.0
                    '''
                  }
            }
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                // sh 'npm run test'
                echo "Test"

            }
        }
        stage('Build Image') {
            steps {
                sh 'ls'
                }
            }
        }
        stage ('Deploy') {
            steps {
                sh 'ls'
                }
            }
        }
    }
