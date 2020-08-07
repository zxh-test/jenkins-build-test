pipeline {
    agent none

    stages {
        stage('build') {
            agent {label "master"}
            tools {maven 'mv3.6.3'}
            steps {
                echo '=========build================'
                sh "mvn clean package spring-boot:repackage"
                sh "printenv"
            }
            post{
            success{
                    echo "========build executed successfully========"
                }
            }
        }
        
        stage("deploy"){
            agent {label "my-mac"}
            steps{
                echo '=========deploy================'
            }
        }
    }
}

