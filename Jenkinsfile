pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                echo 'docker build -t kveerabhadra/adservice:v1 .'
            }
        }
        stage ('push to docker hub'){
            script{
                withDockerRegistry(credentialsId: 'Docker-cred') {
                 // some block
                 sh 'docker push kveerabhadra/adservice:v1 '
                }
            }
        }
    }
}
