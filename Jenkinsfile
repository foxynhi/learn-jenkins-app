pipeline {
    agent any

    stages {
        stage('hello') {
            steps {
                bat 'call npm -v'
                bat 'call npm ci'
                bat 'call npm run build'            
            }
        }
    }
}
