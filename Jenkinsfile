pipeline {
    agent any
    
    stages{
        stage ('docker image') {
            steps{
                sh 'docker build -t python:v1 .' 
            }
            
        }
        
        stage ('delete previous container') {
            steps{
                sh 'docker rm -f python'
            }
        }
        
        stage ('docker container') {
            steps{
                sh 'docker run -t -it --name python -p 5000:5000 python:v1'
            }
        }
    }
}
