// se crea un archivo en /var/fichero.txt en el sistema de ficheros del contenedor ejecutado en la primera fase y se comprueba si en la segunda fase éste sigue existiendo
pipeline {
    agent {
        docker { image 'ubuntu:jammy' }
    }

    stages {
        stage ('Crear el fichero') {
            steps {
                sh 'hostname'
                sh 'echo "un fichero cualquiera" > /var/fichero.txt'
            }
        }

        stage('Comprobar si el fichero sigue estando') {
            steps {
                sh 'hostname'
                sh 'ls /var | grep fichero'           
            } 
        }
    }
}