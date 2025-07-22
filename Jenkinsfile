pipeline {
    agent any

    stages {
        stage('hello') {
            steps {
            bat '''
                call npm ci
                call npm run build
                dir dist
            '''
            }
        }
    }
}
