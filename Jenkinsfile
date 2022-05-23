 pipeline {
    agent any 
    environment {
        
        registry = "iahmed99/instabug-cahllenge"
        registryCredential = 'docker-hub'
        dockerImage = 'instabug-cahllenge'
    }
    
    stages {
        stage('Cloning Git') {
            steps {
                git'https://github.com/IAhmed99/Instabug-Infrastructure-Internship-Cahllenge-2022' 
            }
        }
    
    // Build Docker images
    stage('Building image') {
      steps{
        script {
          dockerImage = docker.build registry
        }
      }
    }
    
     // Push Dokcer Image 
    stage('Upload Image') {
     steps{    
         script {
            docker.withRegistry( 'instabug-cahllenge', registryCredential ) {
            dockerImage.push()
            }
        }
      }
    }