pipeline {
    agent any

    stages {
        stage('hello') {
            steps {
            bat 'call npm ci || echo "npm ci failed but continuing"'
            bat 'call npm run build'
            bat 'npm install -g serve'
            bat 'serve -s build'
            
            }
        }
    }
}
