pipeline {
    agent none
    tools{
        maven 'mv3.6.3'
    }

    stages {
        stage('build') {
            agent {label "master"}
            steps {
                echo '=========build================'
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
                echo '=========build================'
            }
        }
    }
}

