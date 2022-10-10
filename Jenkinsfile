pipeline{
    agent any
    stages{
        stage("checkout"){
            steps{
                git "https://github.com/sbtalk71/assessment-aws-docker.git"
            }
        }
        
         stage("package"){
            steps{
            sh "mvn package"
            }
        }
        
        stage("docker_build"){
            steps{
            sh "sudo docker build -t empdata:$BUILD_NUMBER ."
            }
        }
        
    }
   
}