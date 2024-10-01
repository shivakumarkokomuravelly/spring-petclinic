pipeline {
    agent any 
    stages {
        stage('clone the project') {
            steps {
                git branch: 'main ', url: 'https://github.com/shivakumarkokomuravelly/spring-petclinic.git'
            }
        }
        stage('Building the code'){
            steps{
                sh 'mvn package'
            }
        }
        stage('archiving artifacts'){
            steps{
                archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
            }
        }
        stage('displaying unit test results'){
            steps{
                junit stdioRetention: '', testResults: 'target/surefire-reports/*.xml'
            }
        }

    }
}
