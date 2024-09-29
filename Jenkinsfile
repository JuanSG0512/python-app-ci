pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Clonar el repositorio de GitHub
                git 'https://github.com/JuanSG0512/python-app-ci.git'
            }
        }
        stage('Install Python') {
            steps {
                // Instalar Python en el entorno de Jenkins
                sh 'sudo apt-get update'
                sh 'sudo apt-get install python3 -y'
                sh 'sudo apt-get install python3-pip -y'
            }
        }
        stage('Run Tests') {
            steps {
                // Ejecutar las pruebas unitarias
                sh 'python3 -m unittest test_app.py'
            }
        }
    }
}
