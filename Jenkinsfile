pipeline {
    agent any
    stages {
        stage('Preparar Entorno') {
            steps {
                echo 'Instalando herramientas de Docker dentro de Jenkins...'
                // Esto instala el comando docker dentro del contenedor de Jenkins temporalmente
                sh 'apt-get update && apt-get install -y docker.io'
            }
        }
        stage('Descargar Código') {
            steps {
                echo 'Clonando el repositorio...'
                checkout scm
            }
        }
        stage('Construir Imagen Docker (Build)') {
            steps {
                echo 'Construyendo el contenedor seguro...'
                // Ahora el comando 'docker' ya existirá por el paso anterior
                sh 'docker build -t mi-app-segura:latest .'
            }
        }
    }
}
