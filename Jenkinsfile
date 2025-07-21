pipeline {
    agent any

    stages {
        stage('hello') {
            agent {
                docker {
                    image 'node:20-alpine' // Switch to LTS version
                    reuseNode true
                    args '-v ${WORKSPACE}/npm-logs:/home/node/.npm/_logs' // Mount logs
                }
            }
            steps {
                sh '''
                    ls -la
                    node --version
                    npm --version
                    npm cache clean --force
                    npm ci || (cat /home/node/.npm/_logs/*.log && exit 1)
                    npm run build
                '''
            }
        }
    }
}