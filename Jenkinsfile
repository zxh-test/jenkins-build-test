pipeline {
    agent any
    tools {maven 'mv3.6.3'}

    stages {
        stage('build') {
            agent {label "master"}
            steps {
                echo '=========build================'
                //sh "mvn clean package spring-boot:repackage"
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

