pipeline {
    agent any

    stages {
        stage('hello') {
            steps {
                sh 'npm -v'
                sh 'npm ci'
                sh 'npm run build'            
            }
        }
    }
}
