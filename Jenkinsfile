pipeline {
    agent any
    
    stages {
        stage('cloning the repo'){
            steps{
              git branch: 'main', url: 'https://github.com/shivakumarkokomuravelly/spring-petclinic.git'
            }
        } 
        stage('Build') {
            steps {
                sh 'mvn package'
            }
        }
        stage('download artifacts') {
            steps {
                archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
            }
        }
        
    }


}
