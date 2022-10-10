pipeline{
    agent any
    stages{
        stage("checkout"){
            steps{
                git "https://tools.publicis.sapient.com/bitbucket/scm/psiaug/assessment-aws-docker.git"
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