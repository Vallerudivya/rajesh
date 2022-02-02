pipeline {
    agent any

    stages {
        stage('countinous download') {
            steps {
                git 'https://github.com/boxfuse/boxfuse-sample-java-war-hello.git'
            }
        }
        stage('countinous build') {
            steps {
                sh 'mvn install'
            }
        }
        stage('countinous depolyment') {
            steps {
                sh 'sshpass -p "divya" scp target/hello-1.0.war root@172.17.0.4:/var/lib/apache-tomcat-9.0.56/webapps'
            }
        }
    }
}

