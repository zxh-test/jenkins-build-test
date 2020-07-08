pipeline{
    agent any
    tools {
		maven 'mnv-3.6.3'
    }
    options{
		buildDiscarder(logRotator(numToKeepStr: '10'))
    }
    stages{
        stage("build"){
            steps{
                echo "hello world"
		        sh 'pwd'
		        sh "mvn clean package -Dmaven.test.skip=true"
		        sh "printenv" //将环境变量打印到console中
            }
        }
        stage("Example"){
            steps{
                echo "Running ${env.BUILD_NUMBER} on ${env.JENKINS_URL}" //方法1
                echo "Running $env.BUILD_NUMBER on $env.JENKINS_URL" //方法2
                echo "Running ${BUILD_NUMBER} on ${JENKINS_URL}" //方法3
            }
        }
        
    }
    post{
        always{
            cleanWs()
        }
    }
}
