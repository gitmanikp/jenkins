    pipeline {
        agent {
                docker {
                    image 'java17-maven'
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
                }
            }
        }
    }