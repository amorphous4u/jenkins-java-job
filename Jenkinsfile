pipeline {
    agent any

     stages {
        stage('Build') { 
            steps { 
                git 'https://github.com/amorphous4u/jenkins-java-job.git' 
            }
        }
        stage('Test'){
            steps {
                sh 'hostname'
            }
        }
        stage('Deploy') {
            steps {
                sh 'uname -a'
            }
        }
    }
}

