#!/usr/bin/env groovy
import groovy.json.JsonOutput

pipeline {
    agent any

    options {
        disableConcurrentBuilds()
    }
    
    triggers {
        cron('H * * * *') // run once every hour
    }
    
    environment {
    }

    stages {
        stage('configure') {
            steps {
                sh 'echo "hello carter"'
            }
        }
    }

    post {
        always {
            deleteDir()
            cleanWs()
        }
    }
}