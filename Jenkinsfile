pipeline {
    agent any
    
    stages {
        stage('Clone repository') {
            steps {
                script {
                    // Define las credenciales para acceder al repositorio Git
                    withCredentials([usernamePassword(credentialsId: '4dca1759-e37f-42e9-9e56-49ce02772049' , usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) {
                        // Clonar el repositorio Git usando las credenciales
                        git credentialsId: '4dca1759-e37f-42e9-9e56-49ce02772049' , 'url: https://github.com/Leandritonica92/nodejs-helloworld-api.git'
                    }
                }
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
