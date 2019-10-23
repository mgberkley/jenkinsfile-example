pipeline {
    agent any
    parameters {
        string(name: 'year', defaultValue: '19', description: 'year')
        string(name: 'currentSprint', defaultValue: '99', description: 'Sprint')
        string(name: 'emergencyRelease', defaultValue: '0', description: 'Hotfix=1')
        string(name: 'application', defaultValue: 'myAPP', description: 'appname')
        
    }
    stages {
        stage('SetBUILD') {
            steps {
                echo "${params.application}.${params.year}.${params.currentSprint}.${params.emergencyRelease}.${env.BUILD_ID}"
            }
        }
        stage('Build') {
            steps { 
                echo 'running....'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploying...'
            }
        }
    }
}
