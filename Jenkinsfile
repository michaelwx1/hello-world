/* Requires the Docker Pipeline plugin */
pipeline {
    stage('Initialize'){
        def dockerHome = tool 'my_docker'
        env.PATH = "${dockerHome}/bin:${env.PATH}"
    }
    agent { docker { image 'python:3.12.4-alpine3.20' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
                sh 'python jenkins_learn.py'
            }
        }
    }
}