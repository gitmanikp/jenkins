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
                    // Execute Java application
                    sh 'java -jar target/jenkins-0.0.1-SNAPSHOT.jar'
                    sh 'pkill -f "java -jar target/jenkins-0.0.1-SNAPSHOT.jar"'
                }
            }
        }
    }