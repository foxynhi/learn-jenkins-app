pipeline {
    agent any

    stages {
        stage('hello') {
            steps {
            bat '''
                npm ci || cat /home/node/.npm/_logs/*-debug*.log
                npm run build
            '''
            }
        }
    }
}
