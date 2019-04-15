pipeline {
    agent any
    parameters {
        string (name:'test',
        defaultValue: 'hello',
        description: 'test string in git')
    }
    stages {
        stage('test param') {
            steps {
                bat 'echo ${params.test}'
            }
        } 
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