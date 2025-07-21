pipeline {
    agent any

    stages {
        stage('hello') {
            agent {
                docker{
                    image 'node:22-alpine'
                    reuseNode true
                }
            }
            steps {
            sh '''
                ls -la
                touch /home/node/.npm/_logs/2025-07-21T04_37_09_128Z-debug-0.log
                node --version
                npm --version
                npm ci
                npm run build
            '''
            }
        }
    }
}
