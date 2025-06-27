pipeline { 
    agent any 
    stages { 
        stage('Checkout') { 
            steps { 
                git 'https://github.com/mounikamunji/SimpleJavaApp.git' 
            } 
        } 
        stage('Build Docker Image') { 
            steps { 
                script { 
                    dockerImage = docker.build("mounikamunji/simplejavaapp:latest") 
                } 
            } 
        } 
        stage('Run Docker Container') { 
            steps { 
                script { 
                    docker.image("mounikamunji/simplejavaapp:latest").run() 
                } 
            } 
        } 
    } 
} 
