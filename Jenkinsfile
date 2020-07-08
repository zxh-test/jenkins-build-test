pipeline{
    agent any
    tools {
		maven 'mnv-3.6.3'
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
    }
}
