pipeline { 
    agent any 
ECHO is on.
    stages { 
        stage('Checkout') { 
            steps { 
                git 'https://github.com/mounikamunji/SimpleJavaApp.git' 
            } 
        } 
ECHO is on.
        stage('Build Docker Image') { 
            steps { 
                script { 
                    dockerImage = docker.build("mounikamunji/simplejavaapp:latest") 
                } 
            } 
        } 
ECHO is on.
        stage('Run Container') { 
            steps { 
                script { 
                    docker.image("mounikamunji/simplejavaapp:latest").run() 
                } 
            } 
        } 
    } 
} 
