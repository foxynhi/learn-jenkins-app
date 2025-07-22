pipeline {
    agent any

    stages {
        stage('hello') {
            agent {
                docker{
                    image 'node:20-alpine'
                    reuseNode true
                }
            }
            steps {
                sh 'npm -v'       
            }
        }
    }
}
