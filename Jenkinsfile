pipeline {
    agent any
    
    stages {
        stage('Clone repository') {
            steps {
                git 'https://github.com/edgaregonzalez/nodejs-helloworld-api.git'
            }
        }
        
        stage('Install dependencies') {
            steps {
                sh 'npm install'
            }
        }
        
        stage('Run tests') {
            steps {
                sh 'npm test'
            }
        }
        
        stage('Start server') {
            steps {
                sh 'npm start &'
                // Espera unos segundos para asegurarse de que el servidor se inicie completamente
                sh 'sleep 10'
            }
        }
        
        stage('Make request') {
            steps {
                sh 'curl http://localhost:3000'
            }
        }
    }
    
    post {
        always {
            // Detener el servidor después de que se complete el pipeline
            sh 'pkill node'
        }
    }
}
