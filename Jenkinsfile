pipeline {
    agent any
    parameters {
        string (name:'BRANCH',
        defaultValue: 'master',
        description: 'Branch SVC Git')
    }
    stages {
        stage('Restore') {
            steps {
                bat 'dotnet restore'
            }
        } 
        stage('Build') {
            steps {
                bat 'dotnet build'
            }
        }
    }
}