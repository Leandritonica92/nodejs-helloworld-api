pipeline {
    agent any
    
    stages {
        stage('Clone repository') {
            steps {
                git 'https://github.com/TU_USUARIO/nodejs-helloworld-api.git'
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
                script {
                    // Espera un poco para asegurarse de que el servidor se haya iniciado correctamente!
                    sleep(10)
                }
            }
        }
        
        stage('Make a request') {
            steps {
                sh 'curl http://localhost:3000'
            }
        }
    }
}
