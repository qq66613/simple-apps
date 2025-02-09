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
                sh 'npm install' //for Builds Apps For Reposi
            }
        }
        //Proses Copy Env
        stage('Copy env') {
            steps {
                sh 'cp -p /home/ubuntu/hari-1/simple-apps/.env .' // Copy Env
            }
        }
        //Proses Test Apps
        stage('Testing Apps') {
            steps {
                sh 'npm test' // for test
            }
        }
        //Proses scaning apps
        stage('Scanning Apps') {
            steps {
                sh 'sonar-scanner   -Dsonar.projectKey=simple-apps   -Dsonar.sources=.   -Dsonar.host.url=http://172.23.5.20:9000   -Dsonar.login=sqp_32f12c06ea2d0f55536904722409d6d6a3f979ac'
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