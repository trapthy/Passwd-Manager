pipeline {
    agent any


    stages {
        stage('Checkout') {
            steps {
                script{

                
                git branch: "master",
                    credentialsId: 'git',
                    url: 'https://trapthyshetty@github.com/trapthy/Passwd-Manager.git'
                }

            }
        }
    }
}
