pipeline {
    //Jobs akan di jalanakan pada server devops 1 -> root
    agent {
        node  {
            label 'devops1-kiki'
        }
    }
    //Step SDLC
    stages {
        //Proses Build apps dari repo
        stage('Build Apps') {
            steps {
                echo 'Build Apps'
            }
        }
        //Proses Test Apps
        stage('Testing Apps') {
            steps {
                echo 'Testing Apps'
            }
        }
        //Proses scaning apps
        stage('Scanning Apps') {
            steps {
                echo 'Scanning Apps'
            }
        }
        stage('Builds Images') {
            steps {
                echo 'Builds Images'
            }
        }
        stage('Deploy Images') {
            steps {
                echo 'Deploy Images'
            }
        }
        stage('Publish Images') {
            steps {
                echo 'Publish Images'
            }
        }
    }
}