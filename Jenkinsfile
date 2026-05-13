pipeline {
    agent any
    stages {
        stage('Descargar Código') {
            steps {
                echo 'Clonando el repositorio desde GitHub...'
                // RECUERDA: Cambia TU_USUARIO por tu nombre de GitHub en la URL de abajo
                git branch: 'desarrollo', url: 'https://github.com/Franxopanxo/proyecto-devsecops.git'
            }
        }
        stage('Construir Imagen Docker (Build)') {
            steps {
                echo 'Construyendo el contenedor seguro...'
                sh 'docker build -t mi-app-segura:latest .'
            }
        }
    }
}