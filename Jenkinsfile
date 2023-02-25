pipeline {
  agent any
  stages {
    stage('Install_Dependencies') {
      agent any
      steps {
        sh '''sh \'\'\' wget https://packages.microsoft.com/config/ubuntu/22.10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
                        sudo dpkg -i packages-microsoft-prod.deb
                        sh rm packages-microsoft-prod.deb  
                        sudo apt update && \\
                        sudo apt install -y dotnet-sdk-6.0
                        sudo apt-get update && \\
                        sudo apt-get install -y aspnetcore-runtime-7.0
                    \'\'\''''
      }
    }

  }
}