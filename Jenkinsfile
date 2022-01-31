pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
             sh 'docker build -t hello_world_apache_php .'
             sh 'docker run -d --rm -p 8089:80 hello_world_apache_php'
            }
        }
        stage('Test'){
            steps{
                sh 'wget http://localhost:8089/'
                sh 'wget http://www.joelmmsystem.com/'
            }
        } 
}
}