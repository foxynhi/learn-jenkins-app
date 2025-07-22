pipeline {
    agent any

    stages {
        stage('hello') {
            steps {
            bat 'call npm ci || echo "npm ci failed but continuing"'
            bat 'call npm run build'            
            }
        }
    }
}
