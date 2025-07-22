pipeline {
    agent any

    stages {
        stage('hello') {
            steps {
            sh '''
                ls -la
                node --version
                npm --version
                npm ci || cat /home/node/.npm/_logs/*-debug*.log
                npm run build
            '''
            }
            post {
                success {
                    echo 'Build succeeded!'
                }
                failure {
                    echo 'Build failed.'
                }
            }
        }
    }
}
