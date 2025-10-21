pipeline {
    agent any

    tools {
      jdk 'jdk-17'
      maven 'maven'
    }
    
    stages {
        stage('Maven') {
            steps {
                script {
                    echo "Maven comlie and test for code coverage"
                        sh 'mvn clean package'
                }
            }
        }
        stage('Nexus') {
            steps {
                script {
                    echo "Nexus publishing"
                        sh 'mvn clean package'
                }
            }
        }
        /*
        stage('Build') {
            steps {
                script {
                    echo "docker build"
                        sh 'docker image prune -f'
                        sh 'docker build -t danushvithiyarth/java-app:latest .'
                }
            }
        }
        stage('DockerHub image push') {
            steps {
                script {
                    echo "Image push"
                        sh 'docker login -u "danushvithiyarth" -p "$Docker_pass" docker.io'
                        sh 'docker push danushvithiyarth/java-app:latest'
                }
            }
        }
        */
    }
}

      
