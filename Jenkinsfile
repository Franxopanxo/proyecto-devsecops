pipeline {
    agent any
    stages {
        stage('Descargar Código') {
            steps {
                echo 'Clonando el repositorio...'
                // Jenkins ya descarga el código automáticamente si configuraste el SCM, 
                // pero esto asegura que estamos en la rama correcta.
                checkout scm
            }
        }
        stage('Construir Imagen Docker (Build)') {
            steps {
                echo 'Construyendo el contenedor seguro...'
                // Este comando ahora SÍ debería funcionar
                sh 'docker build -t mi-app-segura:latest .'
            }
        }
    }
}
