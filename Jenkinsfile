pipeline {
    agent any


    stages {
        stage('Checkout') {
            steps {
                script{
                    sh 'echo "Hello"'
                    sh 'ls -ltr'
                    // sh 'pwd'
                }

            }
        }
        stage('Install Packages'){
            steps {
                script {
                    sh 'pip install -r requirements.txt'
                }
            }
          }
        stage('Scan') {
            steps{
            snykSecurity organisation: 'trapthyshetty', projectName: 'trapthy / Passwd-Manager', snykInstallation: 'snyk@latest', snykTokenId: 'c058d01c-fa4f-4572-919a-abb7592ec9d9', snykSecurity additionalArguments: 'snyk test --org=trapthyshetty --file=requirements.txt -- --allow-missing'
            }   
        }
}
}