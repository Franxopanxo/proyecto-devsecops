pipeline {
    agent any
    stages {
        stage('Descargar Código') {
            steps {
                echo 'Clonando el repositorio desde GitHub...'
            }
        }
        stage('Construir Imagen Docker (Build)') {
            steps {
                echo 'Simulando: docker build -t mi-app-segura:latest .'
                echo 'Imagen construida virtualmente con éxito para el pipeline.'
            }
        }
    }
}
