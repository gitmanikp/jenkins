    pipeline {
        agent {
                docker {
                    image 'maven:3.9.6-eclipse-temurin-17-alpine'
                    reuseNode true
                }
            }

        stages {
            stage('Build') {
                steps {
                    // Maven Build
                    sh 'mvn clean install'
                }
            }
            stage('Run') {
                steps {
                    sh 'Running stage RUN'
                }
            }
        }
    }