pipeline {
    agent any

    stages {
        stage('hello') {
            steps {
            bat '''
                call npm ci
                call npm run build
                npm install -g serve
                serve -s build
            '''
            }
        }
    }
}
