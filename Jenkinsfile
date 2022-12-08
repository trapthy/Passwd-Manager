pipeline {
    agent any


    stages {
        stage('Checkout') {
            steps {
                script{
                    sh 'echo "Hello"'
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
            //snykSecurity organisation: 'trapthyshetty', projectName: 'trapthy / Passwd-Manager', snykInstallation: 'snyk@latest', snykTokenId: 'c058d01c-fa4f-4572-919a-abb7592ec9d9'
            sh ' snyk test --org=trapthyshetty --file=requirements.txt -- --allow-missing '
            // snykSecurity( 
            //         snykInstallation: 'snyk@latest', 
            //         snykTokenId: 'c058d01c-fa4f-4572-919a-abb7592ec9d9', 
            //        // monitorProjectOnBuild: false, // snyk-filter is not supported with monitor, so this should be set to false.
            //        // failOnIssues: 'false', // if the build fails in the snykSecurity step, snyk-filter will not run, which is why failOnIssues is set to false.
            //        // additionalArguments: '--json-file-output=all-vulnerabilities.json'
            //     )
            }   
        }
}
}