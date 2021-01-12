pipeline {
    environment {
        DOCKER_TAG = getDockerTag
    }
    agent any
    stages {
        stage('Build Docker Image'){
            steps{ 
                sh "docker build -t musbau8/node-app:$(DOCKER_TAG)"

            }
        }
    }
}
def getDockerTag (){
    def tag = sh script: 'git rev-parse HEAD',returnStdout:true
    return tag
}
