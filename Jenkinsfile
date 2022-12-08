pipeline {
    agent any


    stages {
        stage('Checkout') {
            steps {
                script{
                sh 'echo "Hello"'
                sh 'ls -ltr'
                sh 'pwd'
                }

            }
            stage('Install Packages'){
                steps {
                script {
                    sh 'pip -r requirements.txt'
                }
            }
            }
        }
    }
}
